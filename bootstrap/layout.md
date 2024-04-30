---
title: Layout
description: 
date: 2020-01-20
duration: ~10 mins
layout: layouts/post.njk
---

###### Containers

- .container, which sets a max-width at each responsive breakpoint
- .container-fluid, which is width: 100% at all breakpoints
- .container-{breakpoint}, which is width: 100% until the specified breakpoint.

###### Task 1: Add Container

- Our default .container class is a responsive, fixed-width container, meaning its max-width changes at each breakpoint.
  
``` html
  <div class="container">
    Welcome 
  </div>
```

###### Task 2: Add Container Fluid

- Use .container-fluid for a full width container, spanning the entire width of the viewport.
  
``` html
  <div class="container-fluid">
    Welcome
  </div>
```
