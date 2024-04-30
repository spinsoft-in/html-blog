---
title: LocalStorage - 4
description: This is a post 
date: 2020-02-04
duration: ~20 mins
sections: Task 1
layout: layouts/post.njk
---

## Search data in LocalStorage


###### Prerequiste: Create users array and store users data

```js
    let user1 = { id: 101, name:"Sachin" , email:"sachin@gmail.com", password:"pass123" };
    let user2 = { id: 102, name:"Dhoni" , email:"dhoni@gmail.com", password: "pass123" };
    let users = [ user1, user2 ];
    localStorage.setItem("USER", JSON.stringify(users));
    let usersData = JSON.parse(localStorage.getItem("USERS")) || [];
```

###### Task 1: Search a user exists for the given inputEmailId

```js
    let inputEmailId = "sachin@gmail.com";
    let index = usersData.findIndex(obj=>obj.email == inputEmailId);
    console.log(index);
    if(index == -1) {
        console.log("Email not exists");
    }
    else{ 
        console.log("Email exists at index" , index);
    }

```

Note: findIndex returns the index if data is matched else it will return -1

###### Task 2: Search based on multiple input fields

```js
    let inputEmailId = "sachin@gmail.com";
    let inputPassword = "pass1233";
    let index = usersData.findIndex(obj=>obj.email == inputEmailId && obj.password == inputPassword);
    console.log(index); 
```

Note: In the above example, I have given invalid password, so no records matched it will return -1.

###### Task 3: Search the data, if not matched print "Invalid Credentials", else store the matched in localStorage.

```js
    let inputEmailId = "sachin@gmail.com";
    let inputPassword = "pass1233";
    let user = usersData.find(obj=>obj.email == inputEmailId && obj.password == inputPassword);
    console.log(user);
    if(user==null){
        console.log("Invalid Login Credentials");
    }
    else{
        localStorage.setItem("LOGGED_IN_USER", JSON.stringify(user));
    }
```

Note: find will return the first matched record, else it will return null