---
title: Constants
description: This is a post on My Blog about agile frameworks.
date: 2020-11-03
duration: ~10 mins
layout: layouts/post.njk
---

###### Prerequisite:

``` js
   // Variable ( name ) values can be update with new value.
   let name = 'Naresh';
   name = 'Siva';
   console.log(name);
   // Output: Siva
```

###### Task 1: Declare constant variables and update value

```js
  // Constant Variable (department) value cannot be modified. 
   const department = 'CSE';
   department = 'IT'; // It should throw error
   console.log(department);
```

##### Questions #1:
- When you modify constant variable value, what is the error you will get ?


```js
    Uncaught TypeError: Assignment to constant variable.
```