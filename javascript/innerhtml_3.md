---
title: InnerHTML - 3
description: This is a post on My Blog about agile frameworks.
date: 2020-01-12
duration: ~20 mins
layout: layouts/post.njk
---

###### Prerequisite 1: Design a HTML page with a table with sample dataset

```html
    <h3> Users </h3>
    <table border="1">
        <thead>
            <tr> <th>Id</th><th> Name </th> </tr>
        </thead>
        <tbody id="users-table">
        </tbody>
    </table>
```


##### Task 1: Display the table contents in console

```js
    let tbody = document.querySelector("#users-table");
    console.log(tbody); 
```

###### Task 2: Iterate users data and add the user details in table

```js
    tbody.innerHTML = ""; //clear the tbody contents
    let users = [{id:101, name:"Sachin"} , {id:102, name:"Virat" } , {id: 103, name:"Dhoni"}];
    console.log(users);
    let content = "";
    for(let user of users){
        content += `<tr><td>${user.id}</td><td>${user.name}</td></tr>`;
    }
    console.log(content);
    tbody.innerHTML = content;
```
Note: Used Template Literal Concept - `${user.id}`
