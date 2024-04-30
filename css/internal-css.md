---
title: Internal CSS
description: 
date: 2020-11-03
duration: ~10 mins
day: 1
tags:
  - css
layout: layouts/post.njk
---

## Internal CSS

* CSS enclosed in `<style></style>` tags within an HTML document functions like an external stylesheet, except that it lives in the HTML document it styles instead of in a separate file, and therefore can only be applied to the document in which it lives. 

```html
 <head>
 <style>
        h1 {
            color: green;           
        }       
 </style>
 </head>
 <body>
    <h1>Hello world!</h1>
 </body>
 ```
* Reference: Section 1.2