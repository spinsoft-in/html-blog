---
title: Classname Selectors
description: 
date: 2020-11-03
duration: ~10 mins
day: 1
tags:
  - css
layout: layouts/post.njk
---

## Classname Selectors

 * The class name selector select all elements with the targeted class name. 
 * For example, the class name `.warning` would select the following `<div>` element:

 ```html
    <div class="warning">
        <p>This would be some warning copy.</p>
    </div
 ```

 ```css
    .important {
        color: orange;
    }
    .warning {
        color: blue;
    }
    .warning.important {
        color: red;
    }
 ```

 ```html
    <div class="warning">
        <p>This would be some warning copy.</p>
    </div>
    <div class="important warning">
        <p class="important">This is some really important warning copy.</p>
    </div>
 ```

 *  In this example, all elements with the `.warning` class will have a `blue` text color, elements with the `.important` class
 with have an `orange` text color, and all elements that have both the `.important` and `.warning` class name will have a  red text color.


 *  Notice that within the CSS, the .warning.important declaration did not have any spaces between the two class
 names. This means it will only find elements which contain both class names warning and important in their class
 attribute. Those class names could be in any order on the element.
 If a space was included between the two classes in the CSS declaration, it would only select elements that have
 parent elements with a .warning class names and child elements with .important class names.

 * Reference: Section 4.6

