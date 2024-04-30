---
title: Routing - 1
description: This is a post 
date: 2020-02-01
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: RoutingModule 

``` js
   declartions: [
       ....
       AppRoutingModule

   ]
   
```

###### Task 2: Add router outlet

``` js
   <router-outlet></router-outlet>
```


###### Task 3: Add Routes

``` js
   routes = [
       {path:'home', component:HomeComponent},
       {path:'login', component:LoginComponent},
       {path:'', redirectTo:'login', pathMatch:'full'}

   ];
```


###### Task 4: Add Router Link

``` html
  <a routerLink="login">Login</a> 
```
(or)
```html
  <button type="button" routerLink="login"> Login </button>
```

###### Task 4: Test the Route URL

``` js
   http://localhost:4200/login
```

###### Task 5: Navigate to route

``` js
  constructor(private router:Router) { }

  ....
  this.router.navigate(['login']);
  //or
  this.router.navigateByUrl('login');
```


###### Task 6: Get Router Params
```js
routes = [
    ....
    { path:"users/:userId", component:UserComponent }
]
```

``` js
  userId:number;
  constructor(private route:ActivatedRoute) { 
      this.route.params.subscribe(params=>{
          this.userId = params["userId"];
          console.log("UserId:" + this.userId);
      });
  }

```
###### Task 6.1: Test Router Params

``` js
 http://localhost:4200/users/123

```

###### Task 6.2: Navigate Route with params

``` js
  let userId = 123;
  this.router.navigate(['users/' +userId]);
```


###### Task 7: Get Router Query Params
```js
routes = [
    ....
    { path:"user", component:ViewUserComponent }
]
```

``` js
  userId:number;
  constructor(private route:ActivatedRoute) { 
      this.route.queryParams.subscribe(params=>{
          this.userId = params["userId"];
          console.log("UserId:" + this.userId);
      });
  }

```
###### Task 7.1: Test Router Query Params

``` js
 http://localhost:4200/user?userId=123

```
