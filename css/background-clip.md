---
title: Background Clip
description: 
date: 2020-11-03
duration: ~10 mins
day: 5.10
tags:
  - css
layout: layouts/post.njk
---

## Background Clip
 Definition and Usage: The 
background-clip property specifies the painting area of the background.
 Default value: `border-box`

 **Values**
 
 * `border-box` is the default value. This allows the background to extend all the way to the outside edge of the
 element's border.
 * padding-box clips the background at the outside edge of the element's padding and does not let it extend
 into the border;
 * `content-box` clips the background at the edge of the content box.
 * `inherit` applies the setting of the parent to the selected element


 ```css
  .example {
    width: 300px;
    border: 20px solid black;
    padding: 50px;
    background: url(https://static.pexels.com/photos/6440/magazines-desk-work-workspace-medium.jpg);
    background-repeat: no-repeat;
  }
  .example1 {}
  .example2 { background-origin: border-box; }
  .example3 { background-origin: content-box; }
 ```

 ```html
  <p>No background-origin (padding-box is default):</p>
  <div class="example example1">
  <h2>Lorem Ipsum Dolor</h2>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
  tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
  <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut
  aliquip ex ea commodo consequat.</p>
  </div>
  <p>background-origin: border-box:</p>
  <div class="example example2">
  <h2>Lorem Ipsum Dolor</h2>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
  tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
  <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut
  aliquip ex ea commodo consequat.</p>
  </div>
  <p>background-origin: content-box:</p>
  <div class="example example3">
  <h2>Lorem Ipsum Dolor</h2>
  36
  GoalKicker.com – CSS Notes for Professionals
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
  tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
  <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut
  aliquip ex ea commodo consequat.</p>
  </div>
 ```

 * Reference: Section 5.10
