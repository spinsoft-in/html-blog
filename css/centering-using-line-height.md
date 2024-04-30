---
title: Centering - Using line-height
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

## Using line-height

*   You can also use `line-height` to center vertically a single line of text inside a container 

```html
  <div>Hello</div
```

```css
 div {
    height: 200px;
    line-height: 200px;
 }
```

* That's quite ugly, but can be useful inside an <input /> element. 
* The `line-height` property works only when the  text to be centered spans a single line. 
* If the text wraps into multiple lines, the resulting output won't be centered.


#### Additional Articles
* Vertical align anything with 3 lines of code
* Centering in relation to another item
* Ghost element technique (Michał Czernow's hack)
* Centering vertically and horizontally without worrying about height or width
* Vertically align an image inside div
* Centering with fixed size
* Vertically align dynamic height elements
* Horizontal and Vertical centering using table layout