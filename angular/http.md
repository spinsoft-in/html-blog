---
title: HTTP
description: 
date: 2020-11-05
duration: ~30 mins
tags:
layout: layouts/post.njk
---

###### Prerequisite: Create User Service

``` js
  ng generate service user
```

```js
    @Injectable({
        providedIn: 'root'
    })
    class UserService {
            constructor() { }
    
            getUsers(){
                let users =[ "Naresh", "Siva"];
                return users;
            }
    }
```

###### Task 1: Import HttpClientModule

```js
    imports: [
        HttpClientModule
    ]
```


###### Task 2: Inject HttpClient in Constructor

```js
   class UserService {
        constructor(private http:HttpClient) {  }
   }
```

###### Task 3: Fetch data from a REST API ( Instead of hardcoded data)

```js
    getUsers(){
        //let users =[ "Naresh", "Siva"];
        //return users;
        let url = "http://localhost:5000/api/users";
        return this.http.get(url);
    }
```

###### Task 3.2: Call Service API

```js
    //in component
    users:any;
    constructor(private userService:UserService){ }

    this.userService.getUsers().subscribe (res=>{
        this.users = res;
        console.log(res);
    });

```

###### Task 3.3: List Http Methods

```js
    this.http.get(url); // List all users
    this.http.post(url,formData); // Add User
    this.http.put(url,formData); // Update User
    this.http.patch(url,formData);// Update partial data e.g change password
    this.http.delete(url); //delete user
```