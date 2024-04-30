---
title: Service
description: 
date: 2020-02-05
duration: ~30 mins
tags:
layout: layouts/post.njk
---

###### Task 1: Create User Service

``` js
  ng generate service user
```

```js
    import { Injectable } from '@angular/core';

    @Injectable({
      providedIn: 'root'
    })
    export class UserService {

      constructor() {
      }
    }

```

###### Task 2: Create getUsers method in UserService

```js
 getUsers(){
     let users =[ "Naresh", "Siva"];
     return users;
 }
```

###### Task 3: Call UserService getUsers method from Component

```js
  users:any;
  constructor(private userService:UserService){
     this.users = this.userService.getUsers();
  }
```


###### Questions

- What is Dependency Injection ?
- How Service object is getting injected to component constructors ?
