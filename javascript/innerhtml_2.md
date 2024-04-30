---
title: InnerHTML - 2
description: This is a post on My Blog about agile frameworks.
date: 2020-01-11
duration: ~20 mins
layout: layouts/post.njk
---

###### Prerequisite 1: Design a HTML page with a table with sample dataset

```html
    <h3> Users </h3>
    <table border="1">
        <thead>
            <tr> <th> Name </th> </tr>
        </thead>
        <tbody id="users-table">
            <tr><td>Sachin</td> </tr>
            <tr><td>Dhoni</td></tr>
        </tbody>
    </table>
        
```


##### Task 1: Display the table contents in console
```js
    let tbody = document.querySelector("#users-table");
    console.log(tbody); // It will return  "<tbody id="users-table"><tr><td>Sachin</td> </tr> <tr><td>Dhoni</td></tr></tbody>"
```

###### Task 2:  Clear the default tbody contents

```js
    tbody.innerHTML = ""; //clear the tbody contents
```


###### Task 3:  Add a new user row 

```js
    let content = "<tr><td>Virat</td></tr>";
    tbody.innerHTML = content;
```

###### Task 4: Add a new user ( data is in JSON object)
```js
    tbody.innerHTML = ""; //clear the tbody contents
    let user = {name:"Virat"};
    let content = `<tr><td>${user.name}</td></tr>`;
    tbody.innerHTML = content;
```
