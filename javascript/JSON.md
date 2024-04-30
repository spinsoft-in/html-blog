---
title: JSON
description: This is a post on My Blog about agile frameworks.
date: 2020-01-15
duration: ~10 mins
layout: layouts/post.njk
---

##### Prerequisite : Storing data in variables

``` js
  let id = 101;
  let name = "Naresh";
  let department = "CSE";  
```

###### Task 1: JSON Data are stored as key and value

``` js
    let user = { id: 101, name:"Naresh", department:"CSE" , password:"pass123"};
    console.log(user);
```
Note: Instead of storing data in individual variables, we can store data as a JSON object.

###### Task 2: Accessing JSON data fields

``` js
    let user = { id: 101, name:"Naresh", department:"CSE", password:"pass123" };
    console.log(user.id + "-" +  user.name + "-" + user.department );
```

###### Task 3: Adding Field to JSON data

``` js
    let user = { id: 101, name:"Naresh", department:"CSE", password:"pass123" };
    console.log(user);
    user["active"] = 1;
    console.log(user);
    console.log(user.active);
```

###### Task 3: Deleting a password property from JSON object.

``` js
    let user = { id: 101, name:"Naresh", department:"CSE", password:"pass123"};
    console.log(user);
    delete user["password"];
    console.log(user);
```

###### Task 4: JSON Methods - Convert JSON object to String ( using JSON.stringify() method)

```js
    let user = { id: 101, name:"Naresh", department:"CSE", password:"pass123"};
    console.log(user);
    let userStr = JSON.stringify(user);
    console.log(userStr);
```

###### Task 5: JSON Methods - Convert JSON String to JSON object (using JSON.parse() method )

```js
    let user = { id: 101, name:"Naresh", department:"CSE", password:"pass123"};
    console.log(user);
    let userStr = JSON.stringify(user);
    console.log(userStr);
    let userObj = JSON.parse(userStr); // Input is JSON String , Output is JSON object.
    console.log(userObj);
```
