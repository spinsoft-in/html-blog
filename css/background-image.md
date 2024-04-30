---
title: Background Image
description: 
date: 2020-11-03
duration: ~10 mins
day: 5.3
tags:
  - css
layout: layouts/post.njk
---

## Background Image

* The background-image property is used to specify a background image to be applied to all matched elements. By
 default, this image is tiled to cover the entire element, excluding margin.


 ```css
    .myClass {
        background-image: url('/path/to/image.jpg');
    }
```

#### To use multiple images as background-image, define comma separated url()

```css
 .myClass {
    background-image: url('/path/to/image.jpg'),
                      url('/path/to/image2.jpg');
 }
```

* The images will stack according to their order with the first declared image on top of the others and so on.

|Value |Result |
|--|--|
 url('/path/to/image.jpg') |Specify background image's path(s) or an image resource specified with data URI
 schema (apostrophes can be omitted), separate multiples by comma|
 |none| No background image|
 |initial| Default value|
 |inherit |Inherit parent's value|
 
 
 #### More CSS for Background Image
 * This following attributes are very useful and almost essential too.

 ```css
 background-size:     xpx ypx | x% y%;
 background-repeat:   no-repeat | repeat | repeat-x | repeat-y;
 background-position: left offset (px/%) right offset (px/%) | center center | left top | right
 bottom
```

* Reference: Section 5.3