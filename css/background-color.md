---
title: Background Color
description: 
date: 2020-11-03
day: 5.1
duration: ~10 mins
tags:
  - css
layout: layouts/post.njk
---

## Background color

*  The transparent, `background-color` property sets the background color of an element using a color value or through keywords, such as inherit or initial.
 * **transparent**, specifies that the background color should be transparent. This is default.
 * **inherit**, inherits this property from its parent element.
 * **initial**, sets this property to its default value.

 * This can be applied to all elements, and `:: first-letter/::first-line `psuedo elements.
 
 * Colors in CSS can be specified by different methods :

```html
 <div>This will have a red background</div
```

### Color Names
```css
    div {
        background-color: red;  /* red */
    }
```

### Hex color codes
*  Hex code is used to denote RGB components of a color in base-16 hexadecimal notation. 
* `#ff0000`, for example, is `bright red`, where the red component of the color is 256 bits (ff) and the corresponding green and blue portions of the color is 0 (00).
* If both values in each of the three RGB pairings (R, G, and B) are the same, then the color code can be shortened into three characters (the first digit of each pairing). 
* `#ff0000` can be shortened to shortened to `#fff`.
* Hex notation is case-insensitive

```css
    body {
        background-color: #de1205; /* red */
    }
    .main {
        background-color: #00f; /* blue */
    }
 ```

 ### RGB / RGBa

 * RGB stands for Red, Green and Blue, and requires of three separate values between 0 and 255, put between brackets, that correspond with the decimal color values for respectively red, green and blue.
 * RGBa allows you to add an additional alpha parameter between 0.0 and 1.0 to define opacity.

 ```css
    header {
        background-color: rgb(0, 0, 0); /* black */
    }
    footer {
        background-color: rgba(0, 0, 0, 0.5); /* black with 50% opacity */
    }
 ```

 ### HSL / HSLa
 *  Another way to declare a color is to use HSL or HSLa and is similar to RGB and RGBa.
 * HSL stands for hue, saturation, and lightness, and is also often called HLS:
 * Hue is a degree on the color wheel (from 0 to 360).
 * Saturation is a percentage between 0% and 100%.
 * Lightness is also a percentage between 0% and 100%.
 * HSLa allows you to add an additional alpha parameter between 0.0 and 1.0 to define opacity

 ```css
    li a {
        background-color: hsl(120, 100%, 50%); /* green */
    }
    #p1 {
        background-color: hsla(120, 100%, 50%, .3); /* green with 30% opacity */
    }
```

###  Interaction with background-image

```css
    body {
        background: red;
        background-image: url(partiallytransparentimage.png);
    }
    body {
        background-color: red;
        background-image: url(partiallytransparentimage.png);
    }
    body {
        background-image: url(partiallytransparentimage.png);
        background-color: red;
        }
    body {
        background: red url(partiallytransparentimage.png);
    }
 ```


 * Reference: Section 5.1
