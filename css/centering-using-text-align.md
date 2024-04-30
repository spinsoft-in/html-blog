---
title: Centering - Using text-align
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

##  Using text-align

*   The most common and easiest type of centering is that of lines of text in an element. 
* CSS has the rule `text-align:center` for this purpose:

```html
  <p>Lorem ipsum</p>
 </div>
```

```css
  p {
    text-align: center;
  }
```
*  This does not work for centering entire block elements. 
* `text-align` controls only alignment of inline content like text in its parent block element.