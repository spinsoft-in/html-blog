---
title: Use Bootstrap via npm
description: 
date: 2020-02-01
duration: ~15 mins
tags:
layout: layouts/post.njk
---


###### Prerequisite: Create Node Project

```js
    mkdir project1
    cd project1
    npm init -y
```

###### Task 1.1: Install Bootstrap

```js
  npm install bootstrap
```

###### Task 1.2 : Check node_modules folder for bootstrap

```js
  node_modules/dist/css/bootstrap.min.css
  node_modules/dist/js/bootstrap.min.js
```

###### Task 1.3: Refer bootstrap in html

```html
    <head>    
        <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
        <script src="node_modules/bootstrap/dist/js/bootstrap.min.js"> </script>  
    </head>
```

###### Task 1.4: Install Jquery ( Bootstrap internally uses jquery )

```js
    npm i jquery
```

```html
    <head>    
        <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
        <script src="node_modules/jquery/dist/jquery.min.js"></script>
        <script src="node_modules/bootstrap/dist/js/bootstrap.min.js"> </script>
    </head>  
```

Note: Jquery must be included before bootstrap.min.js
