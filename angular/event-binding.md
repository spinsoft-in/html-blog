---
title: Event Binding
description: This is a post 
date: 2020-01-15
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Event Binding

- Event binding allows you to listen for and respond to user actions such as keystrokes, mouse movements, clicks, and touches.

```html
    <button (click)="onSave()"> Save </button>
```

```ts
    onSave(){
        alert("Button onSave clicked");
    }
```