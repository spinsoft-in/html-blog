---
title: Remove bullet point in List
description: 
date: 2020-11-03
duration: ~10 mins
day: 2
tags:
  - css
layout: layouts/post.njk
---

#### Remove bullet point in list


```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Menu Example</title>
      <style>
          /* Basic styling for the menu */
          ul {
              list-style-type: none;
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