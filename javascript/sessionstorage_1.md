---
title: sessionStorage - 1
description: This is a post 
date: 2020-02-05
duration: ~20 mins
sections: Task 1

layout: layouts/post.njk
---

###### Task 1: Store a name, userId in sessionStorage
```js
  let firstName='Sachin'; //string
  sessionStorage.setItem("name",firstName);
  let userId = 101; //number
  sessionStorage.setItem("id",userId);
```

Note: In sessionStorage, all the data will be stored as string.

###### Task 2: Retrieve the data from sessionStorage
```js
  let fName = sessionStorage.getItem("name");// It returns "Sachin" as string
  console.log(fName);
  let uId = sessionStorage.getItem("id"); //It returns "101" as string( Not a number)
  console.log(uId);
```
Note: When retrieving data from sessionStorage, it returns all data as string.

###### Task 3: Convert userId string to number
```js
  let userIdStr = sessionStorage.getItem("id");
  let userIdNumber = parseInt(userIdStr); // we need to convert string to number 
```

###### Task 4: Short Syntax to get data from sessionStorage
```js
console.log(sessionStorage.getItem("name"));
console.log(sessionStorage.name);
```

###### Task 5: Remove an item from sessionStorage
```js
  sessionStorage.removeItem("name");
```

###### Task 6: Remove all items from sessionStorage
```js
  sessionStorage.clear();
```

