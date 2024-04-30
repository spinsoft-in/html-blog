---
title: Centering - Using position
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

##  Using position

*  Automatic margins, paired with values of zero for the `left` and `right` or `top` and `bottom` offsets, will center an absolutely positioned elements within its parent.

```html
  <div class="parent">
    <img class="center" src="http://lorempixel.com/400/200/" />
 </div
```

```css
  .parent {
    position: relative;
    height: 500px;
  }
  .center {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
  }
```