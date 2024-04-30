---
title: Background Size
description: 
date: 2020-11-03
duration: ~10 mins
day: 5.5
tags:
  - css
layout: layouts/post.njk
---

## Background Size

* The background-size property enables one to control the scaling of the background-image. 

* It takes up to two values, which determine the scale/size of the resulting image in vertical and and horizontal direction. 

* If the property is missing, its deemed auto in both width and height.
* auto will keep the image's aspect ratio, if it can be determined. The height is optional and can be considered 


Therefore, on a 256 px × 256 px image, all the following 
auto.
 
* `background-size` settings would yield an image with height and width of 50 px:

```css
 background-size: 50px;
 background-size: 50px auto; /* same as above */
 background-size: auto 50px;
 background-size: 50px 50px;
```

* Reference: 5.5

