---
title: Routing - Nested Routes
description: This is a post 
date: 2020-02-02
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: Child Routes

``` js
  routes = [
      { path:'account/:accountNo', component: AccountComponent,
        children:[
            {path:'', component:ViewAccountComponent},
            {path:'transactions', component:ViewTransactionsComponent}
        ]
      }
  ]
```

###### Task 2: Get Parent Route Params

``` js
  accountNo:number;
  this.router.parent.params.subcribe(params=>{
      this.accountNo = params["accountNo"];
  });
```
