---
title: Property Binding
description: 
date: 2020-01-26
duration: ~20 mins
tags:
layout: layouts/post.njk
---


###### Task 1: Display Image 

- app.component.ts
  
```ts
    imageUrl="assets/product1.jpg";
```

- app.component.html
  
```html
    <img [src]="imageUrl"> </img> <!-- Property Binding -->
 ```


 ###### Task 2: Disable Button if form is invalid

 ```html
    <form #f="ngForm">
        <input type="text" name="username" ngModel required>
        <button [disabled]="f.invalid"> Submit </button>
    </form>
```

###### Task 3: Display comments in innerHTML

```ts
    comments = "<p>Text</p>";
```

```html
    <span [innerHTML]="comments"></span>
```
