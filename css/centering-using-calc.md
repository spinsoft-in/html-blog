---
title: Centering - Using calc()
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

## Using calc()

*  The calc() function is the part of a new syntax in `CSS3` in which you can calculate (mathematically) what size/position
 your element occupies by using a variety of values like pixels, percentages, etc. 
 
 * Note: Whenever you use this function, always take care of the space between two values calc(100% - 80px)

```html
   <div class="center"></div>
```

```css
 .center {
    position: absolute;
    height: 50px;
    width: 50px;
    background: red;
    top: calc(50% - 50px / 2); /* height divided by 2*/
    left: calc(50% - 50px / 2); /* width divided by 2*/
 }
```