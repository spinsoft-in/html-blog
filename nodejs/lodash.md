---
title: Use Lodash library 
description: 
date: 2020-02-02
duration: ~10 mins
layout: layouts/post.njk
---


###### Prerequisite : Install Lodash Dependency

- https://www.npmjs.com/package/lodash ( Weekly Downloads - 37M)
  
```js
    npm i lodash
```

###### Task 1: Refer the lodash js

```html
    <script src="node_modules/lodash/lodash.min.js"> </script>
```

###### Task 2: Find unique department names using lodash  ( _uniq)

```js
    let departments  = ["CSE","IT","CSE", "MECH"];
    let uniqueDepartments = _.uniq ( departments);
    console.log(uniqueDepartments);
```