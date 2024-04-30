---
title: ClassName Attribute
description: 
date: 2022-11-03
day: 4
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### How to use class attribute ?

* CSS
```css
  .message { 
    color: green 
  }
```


* In html, we use `class` attribute 

```tsx
  <div class="message">Success</div>
```

* In Next.js, we use `className` attribute,since `class` keyword is reserved.

```tsx
  <div className="message">Success</div>
```