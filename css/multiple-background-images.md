---
title: Multiple Background Image
description: 
date: 2020-11-03
duration: ~10 mins
day: 5.8
tags:
  - css
layout: layouts/post.njk
---

## Multiple Background Image

*  In CSS3, we can stack multiple background in the same element.
 
 ```css
  #mydiv {
    background-image: url(img_1.png), /* top image */
                      url(img_2.png), /* middle image */
                      url(img_3.png); /* bottom image */

    background-position: right bottom,
                         left top,
                         right top;

    background-repeat: no-repeat,
                       repeat,
                       no-repeat;
  }
 ```

 * Images will be stacked atop one another with the first background on top and the last background in the back.

* We can also use background shorthand property for this:

```css
 #mydiv {
  background: url(img_1.png) right bottom no-repeat,
              url(img_2.png) left top repeat,
              url(img_3.png) right top no-repeat;
 }
 ```

 * We can also stack images and gradients:

 ```css
 #mydiv {
  background: url(image.png) right bottom no-repeat,
              linear-gradient(to bottom, #fff 0%,#000 100%);
 }
 ```

 * Reference: Section 5.8