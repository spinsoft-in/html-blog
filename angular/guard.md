---
title: Guard
description: This is a post 
date: 2020-02-03
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

#### Guards

- Use route guards to prevent users from navigating to parts of an app without authorization. The following route guards are available in Angular:

- CanActivate
- CanActivateChild
- CanDeactivate
- Resolve
- CanLoad

s
###### Task 1: Create a guard - AuthGuard 

``` js
    ng generate guard auth
```

```html
    (*) CanActivate
    ( ) CanActivateChild
    ( ) CanDeactivate
    ( ) CanLoad
```

###### Task 2: Auth Guard ( Default code)

``` js
    export class AuthGuard implements CanActivate {

        constructor(private router:Router){ }

        canActivate(
            route: ActivatedRouteSnapshot,
            state: RouterStateSnapshot): Observable<boolean | UrlTree> | Promise<boolean | UrlTree> | boolean | UrlTree {
            
            console.log('AuthGuard');
        
            return true;
        }
        
    }
```


###### Task 3: Implement logic to redirect to login page, if user is not loggedin

``` js
        let user = localStorage.getItem("LOGGED_IN_USER");
        console.log("AuthGuard" , user);  
        if(user){
            console.log("User is LoggedIn", user);
        }
        else{
             console.log("User is not yet LoggedIn");
            //window.location.href="login";
            this.router.navigate(['login']);
        }

```


###### Task 4: Protecting route with guard

``` js
  routes = [
      {path:'create-account', component: CreateAccountComponent,
        canActivate:[AuthGuard]
      }
  ]
```
