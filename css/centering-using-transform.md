---
title: Centering - Using css transform
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

## Centering - Using CSS Transform

* CSS transforms are based on the size of the elements so if you don't know how tall or wide your element is, you can
 position it absolutely 50% from the top and left of a relative container and translate it by 50% left and upwards to
 center it vertically and horizontally.

 ```html
  <div class="container">
    <div class="element"></div>
  </div
 ```

 ```css
  .container {
    position: relative;
  }
  .element {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
 ```
