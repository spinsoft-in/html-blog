---
title: Centering - Using Flexbox
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

## Centering - Using Flexbox


```html
 <div class="container">
  <img src="http://lorempixel.com/400/200" />
 </div>
 ```

 ```css
  html, body, .container {
    height: 100%;
  }    
  .container {
    display: flex;
    justify-content: center; /* horizontal center */
  }
  img {
    align-self: center; /* vertical center */
  }
 ```

 * Example 2

 ```css
  html, body {
    height: 100%;
  }  
  body {
    display: flex;
    justify-content: center; /* horizontal center */
    align-items: center;     /* vertical center */
 }
 ```
 * See Dynamic Vertical and Horizontal Centering under the Flexbox documentation for more details on flexbox and
 what the styles mean.
