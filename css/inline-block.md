---
title: Inline Element
description: 
date: 2020-11-03
duration: ~10 mins
day: 1
tags:
  - css
layout: layouts/post.njk
---

#### Create a List and display items inline 

* Convert block element to inline.

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Inline Element</title>
      <style>          
          li {
              display: inline;              
          }        
      </style>
  </head>
  <body>
    
      <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Services</a></li>
          <li><a href="#">Contact</a></li>
      </ul>
  </body>
  </html>
```