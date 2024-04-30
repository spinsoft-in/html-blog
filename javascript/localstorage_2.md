---
title: LocalStorage - 2
description: This is a post 
date: 2020-02-02
duration: ~20 mins
sections: Task 1
layout: layouts/post.njk
---

###### Prerequiste: Store a name, userId in LocalStorage

```js
  let firstName='Sachin'; //string
  localStorage.setItem("name",firstName);
  let userId = 101; //number
  localStorage.setItem("id",userId);
```

###### Task 1: Instead of storing individual data , store it as an object

```js
  let user1 = {id: 101, name:"Sachin"}; // Object
  localStorage.setItem("LOGGED_IN_USER", user1);  
  console.log(localStorage.LOGGED_IN_USER); 
  //It will return as "[object Object]"  which is not usable.
```

Note: While storing objects, we need to do JSON.stringify() 

###### Task 2.1: Instead of storing individual data , store it as an object

```js
  let user1 = {id: 101, name:"Sachin"}; // Object
  localStorage.setItem("LOGGED_IN_USER", JSON.stringify(user1)); 
  console.log(localStorage.LOGGED_IN_USER); 
  //It will return as "{"id":101,"name":"Sachin"}"  which is usable.
```

###### Task 2.2: Display the user details(id,name)

```js
    let userStr = localStorage.getItem("LOGGED_IN_USER");
    let userObj = JSON.parse(userStr); //We need to convert string to object using JSON.
    console.log(userObj.id +"-" +userObj.name);
    //It returns =>101-Sachin
```
