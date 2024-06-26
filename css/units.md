---
title: Units
description: 
date: 2020-11-03
duration: ~10 mins
day: 7
tags:
  - css
layout: layouts/post.njk
---

## Units

|Unit|  Description|
|--|--|
 |% |Define sizes in terms of parent objects or current object dependent on property|
 |em |Relative to the font-size of the element (2em means 2 times the size of the current font)|
 |rem |Relative to font-size of the root element|
 |vw |Relative to 1% of the width of the viewport*|
 |vh |Relative to 1% of the height of the viewport*|
 |vmin |Relative to 1% of viewport's* smaller dimension|
 |vmax |Relative to 1% of viewport's* larger dimension|
 |cm |centimeters|
 |mm |millimeters|
 |in | inches (1in = 96px = 2.54cm) |
 |px | pixels (1px = 1/96th of 1in)|
 |pt | points (1pt = 1/72 of 1in)|
 |pc | picas (1pc = 12 pt) |
 |s| seconds |(used for animations and transitions)|
 |ms |milliseconds (used for animations and transitions)|
 |ex | Relative to the x-height of the current font 
 | ch| Based on the width of the zero (0) character |
 |fr|  fractional unit (used for CSS Grid Layout)|


 * A CSS distance measurement is a number immediately followed by a length unit (px, em, pc, in, …)
 * CSS supports a number of length measurements units. They are absolute or relative


 ### Additional Articles

 *  Creating scalable elements using rems and ems
 *  Font size with rem
 * vmin and vmax
 * vh and vw

  CSS3 introduced two units for representing size.
 vh, which stands for 
viewport height is relative to 1% of the viewport height
 vw, which stands for 
viewport width is relative to 1% of the viewport width

* using percent %

```bash
( Parent Container`s width ) * ( Percentage(%) ) = Output
```

