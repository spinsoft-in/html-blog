---
title: LocalStorage - 5
description: This is a post 
date: 2020-02-05
duration: ~20 mins
sections: Task 1

layout: layouts/post.njk
---

## Update a specific data in LocalStorage.

###### Task 1.1: Store a user data

```js
    let user = { id: 101, name:"Sachin", active:0 };
    localStorage.setItem("USER",JSON.stringify(user));
```

###### Task 1.2: Update the field from active=0 to active=1 and store it back in localStorage 

```js
    let selectedUser = JSON.parse(localStorage.getItem("USER"));
    console.log(selectedUser);
    //update the field - active from 0 to 1
    selectedUser["active"]=1;
    //write it back to localStorage
    localStorage.setItem("USER", JSON.stringify(user));
```

###### Task 2.1: Store multiple users data

```js
    let user1 = { id: 101, name:"Sachin", active:0 };
    let user2 = { id: 102, name:"Dhoni", active:0 };
    let users = [user1, user2];
    localStorage.setItem("USERS",JSON.stringify(users));
```

##### Task 3.2: Update active field from 0 to 1 for user who has id=102

```js
    let userId = 102; // For this user, we are going to update active from 0 to 1
    //Get users data from LocalStorage.
    let users = JSON.parse(localStorage.getItem("USERS")) || [];
    console.log(users);
```

```js
    let index = users.findIndex(obj=>obj.id == userId ); //It will return index = 1
    let selectedUser = users[index]; // Get the user object 
    console.log(selectedUser);
```

```js
    // update active from 0 to 1
    selectedUser["active"] = 1;
    users[index] = selectedUser; // Assign the updated user object back to array.
```

```js
    //write the updated users array to localStorage
    localStorage.setItem("USERS", JSON.stringify(users));
```