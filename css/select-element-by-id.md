---
title: Select element by Id
description: 
date: 2020-11-03
duration: ~10 mins
day: 2
tags:
  - css
layout: layouts/post.njk
---

## Select element by Id

*  This trick helps you select an element using the ID as a value for an attribute selector to avoid the high specificity of
 the ID selector.

```html
 <div id="element">...</div> 
 ```

 ```css
 #element { ... } /* High specificity will override many selectors */
 ```

```html
    <div id="exampleID">
        <p>Example</p>
    </div>
 ```

 ```css
    #exampleID {
        width: 20px;
    }
 ```

 *  Note: The HTML specs do not allow multiple elements with the same ID

* Reference: Section 4.12