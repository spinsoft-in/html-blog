---
title: LocalStorage - 3
description: This is a post 
date: 2020-02-03
duration: ~20 mins
sections: Task 1

layout: layouts/post.njk
---

###### Prerequiste: Create users array and store users data

```js
    let user1 = { id: 101, name:"Sachin" };
    let user2 = { id: 102, name:"Dhoni" };
    let users = [];
    users.push(user1);
    users.push(user2);
    console.log(JSON.stringify(users));
    // [{"id":101,"name":"Sachin"},{"id":102,"name":"Dhoni"}]
```

###### Task 1: Store users in LocalStorage

```js
    localStorage.setItem("USERS", JSON.stringify(users));
```

###### Task 2: Retrieve users data and display user details

```js
    let usersData = JSON.parse(localStorage.getItem("USERS"));
    console.log(usersData);
    for(let obj of usersData){
        console.log(obj.id + "-" + obj.name);
    }
    //output:
    //101-Sachin
    //102-Dhoni

```

##### Task 3: Add an item to existing Users data in localStorage

```js
    let usersStr = localStorage.getItem("USERS");
    console.log(usersStr);
    // if users data available in localStorage, then do parse else assign an empty array

    let users = usersStr != null ? JSON.parse(usersStr): []; 
    console.log(users);
    let newUser = {id: 103, name:'Virat'};
    users.push(newUser);
    //write the updated users array to localStorage
    localStorage.setItem("USERS", JSON.stringify(users));
```
