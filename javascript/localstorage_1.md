---
title: LocalStorage - 1
description: This is a post 
date: 2020-02-01
duration: ~20 mins
sections: Task 1
layout: layouts/post.njk
---

###### Task 1: Store a name, userId in LocalStorage

```js
  let firstName='Sachin'; //string
  localStorage.setItem("name",firstName);
  let userId = 101; //number
  localStorage.setItem("id",userId);
```

Note: In localStorage, all the data will be stored as string.

###### Task 2: Retrieve the data from localStorage

```js
  let fName = localStorage.getItem("name");// It returns "Sachin" as string
  console.log(fName);
  let uId = localStorage.getItem("id"); //It returns "101" as string( Not a number)
  console.log(uId);
```

Note: When retrieving data from localStorage, it returns all data as string.

###### Task 3: Convert userId string to number

```js
  let userIdStr = localStorage.getItem("id");
  let userIdNumber = parseInt(userIdStr); // we need to convert string to number 
```

###### Task 4: Short Syntax to get data from localStorage

```js
  console.log(localStorage.getItem("name"));
  console.log(localStorage.name);
```

###### Task 5: Remove an item from LocalStorage

```js
  localStorage.removeItem("name");
```

###### Task 6: Remove all items from LocalStorage

```js
  localStorage.clear();
```

