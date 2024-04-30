---
title: Centering - Using margin
description: 
date: 2020-11-03
duration: ~10 mins
day: 6.1
tags:
  - css
layout: layouts/post.njk
---

##  Using margin: 0 auto

*  Objects can be centered by using `margin: 0 auto;` if they are block elements and have a defined width.

```html
 <div class="containerDiv">
 <div id="centeredDiv"></div>
 </div>
 <div class="containerDiv">
 <p id="centeredParagraph">This is a centered paragraph.</p>
 </div>
 <div class="containerDiv">
 <img id="centeredImage"
 src="https://i.kinja-img.com/gawker-media/image/upload/s--c7Q9b4Eh--/c_scale,fl_progressive,q_80,w_
 800/qqyvc3bkpyl3mfhr8all.jpg" />
 </div>
```

```css
  .containerDiv {
    width: 100%;
    height: 100px;
    padding-bottom: 40px;
  }
  #centeredDiv {
    margin: 0 auto;
    width: 200px;
    height: 100px;
    border: 1px solid #000;
  }
  #centeredParagraph {
    width: 200px;
    margin: 0 auto;
  }
  #centeredImage {
    display: block;
    width: 200px;
    margin: 0 auto;
  }
```
