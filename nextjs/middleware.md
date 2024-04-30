---
title: Middleware
description: 
date: 2022-11-03
day: 10
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---


### Create Middleware

* `src/middleware.ts`
* Note: Keep the middleware.ts in `src` folder (not in `app` folder)

```tsx
    "use client";

    import { NextResponse } from 'next/server'
    import type { NextRequest } from 'next/server'

    // This function can be marked `async` if using `await` inside
    export async function middleware(request: NextRequest) {
        
        console.log("Middleware request url: " + request.url);
        const path = request.nextUrl.pathname;
        console.log("Path:" + path);
        //return NextResponse.redirect(new URL('/login', request.url))

        return NextResponse.next();
    }

    // See "Matching Paths" below to learn more
    export const config = {
        matcher: [ "/", "/login"],
    }
```

#### Test url - 1

* http://localhost:3000/

```bash
    Middleware request url: http://localhost:3000/
    Path: /
```

#### Test url - 2

* http://localhost:3000/login

```bash
    Middleware request url: http://localhost:3000/login
    Path: /login
```
