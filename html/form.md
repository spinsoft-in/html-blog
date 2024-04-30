---
title: Forms
description: 
date: 2020-11-03
duration: ~10 mins
tags:
  - HTML
layout: layouts/post.njk
---

###### Task 1: Create Form with action

```html
    <form action="nextpage.html">
        <button>Submit</button>
    </form>
```

###### Task 2: Create Form with action (GET/POST) => Default(GET)
```html
    <form method="GET">
    Name: <input type="text" value="Naresh" >
    <button>Submit</button>
    </form>
```
```html
    <form method="POST">
    Name: <input type="text" value="Naresh" >
    <button>Submit</button>
    
    </form>
```

###### Task 3: Call JavaScript
```html
    <form onsubmit="callfunction()">
    
    </form>
```
