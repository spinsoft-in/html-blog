---
title: Inline CSS
description: 
date: 2020-11-03
duration: ~10 mins
day: 1
tags:
  - css
layout: layouts/post.njk
---

## Inline CSS

* Use inline styles to apply styling to a specific element. 
* Note that this is **not** optimal. 
  * Placing style rules in a `<style>` tag or external CSS file is encouraged in order to maintain a distinction between content and presentation.

```html
 <body>
     <h1 style="color: green; ">Hello world!</h1>
 </body>
 ```

 * Inline styles override any CSS in a `<style>` tag or external style sheet. 
 * While this can be useful in some circumstances, this fact more often than not reduces a project's maintainability.

* Reference: Section 1.4