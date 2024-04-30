---
title: Routing - Protecting Routes
description: This is a post 
date: 2020-02-03
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---


###### Task 1: Protecting route with guard


``` js
  routes = [
      {path:'create-account', component: CreateAccountComponent,
        canActivate:[AuthGuard,RoleGuard]
      }
  ]
```
