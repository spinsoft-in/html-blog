---
title: Middleware Advanced
description: 
date: 2022-11-03
day: 11
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---


### Middleware - Checking paths

* `src/middleware.ts`
* Note: Keep the middleware.ts in `src` folder (not in `app` folder)

```tsx
   
    export async function middleware(request: NextRequest) {
        
        console.log("Middleware request url: " + request.url);
        const path = request.nextUrl.pathname;
        // logic
    }

```

#### 1. Allow Internal Paths

* Exclude Paths
 * `_next` -  Next.js internals
 * `/api` -  all API routes
 * `/static` - static files
```tsx
    const PUBLIC_FILE = /\.(.*)$/;
    if (
        path.startsWith("/_next") || 
        path.startsWith("/api") || 
        path.startsWith("/static") || 
        PUBLIC_FILE.test(path)
    ) {

        return NextResponse.next();
    
    }

```

#### 2. Public Paths

```tsx
    const publicPaths = ["/"];
    const isPublicPath = publicPaths.includes(path);
    if (isPublicPath) {
      return;
    }
```

#### 3. Private Paths

```tsx
    const unAuthenticatedRoute = [
        "/login",
        "/signup",
    ];
    const isUnAuthenticatedPath = unAuthenticatedRoute.includes(path);

```

#### 4. Token Exists Check

* If token exists proceed to the requested page.
* If token not exists, redirect to login page.

```tsx
    const token = request.cookies.get("token")?.value || "";
    console.log("Token:" + token );
    if( token != null && token != "" ){
        return NextResponse.next();
    }else{
         return NextResponse.redirect(new URL("/login", request.nextUrl));
    }
```

* Note: Add additional logic to validate, whether the given token is valid or not.

#### 5. Role Check

```tsx
    const role = localStorage.getItem("role");
    if(role == "ADMIN"){
        return NextResponse.redirect(new URL("/admin/dashboard", req.nextUrl));
    }else if (role=="USER"){
        return NextResponse.redirect(new URL("/user/dashboard", req.nextUrl));
    }else {
        return NextResponse.redirect(new URL("/login", request.nextUrl));
    }
```

* If role is ADMIN, and if the user is requested path contains 'admin' then proceed the request.
* If role is USER, and if the user is requested path contains 'user' then proceed the request.
* Otherwise, redirect to homepage.

```tsx
    if ( role == "ADMIN" && path.includes("admin")) {
        return NextResponse.next();
    } else if ( role == "USER" && path.includes("user")) {
        return NextResponse.next();
    } else {
        return NextResponse.redirect(new URL("/", req.nextUrl));
    }
```

#### Configurations

```tsx
    export const config = {
    matcher: [
            // Auth routes
            "/",
            "/login",    
            "/signup",

            // Admin routes
            "/admin/:path*",

            // user routes
            "/user/:path*",
        ],
    };
```