---
title: Background Attachment
description: 
date: 2020-11-03
duration: ~10 mins
day: 5.9
tags:
  - css
layout: layouts/post.njk
---

## Background Attachment
 
* The background-attachment property sets whether a background image is fixed or scrolls with the rest of the page.

```css
 body {
  background-image: url('img.jpg');
  background-attachment: fixed;
 }
```

|Value |Description|
| scroll |The background scrolls along with the element. This is default.|
| fixed| The background is fixed with regard to the viewport.|
 |local |The background scrolls along with the element's contents.|
 |initial |Sets this property to its default value.|
 |inherit |Inherits this property from its parent element|

 * Reference: Section 5.9