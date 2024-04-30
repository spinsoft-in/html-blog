---
title: Attribute Directives
description: This is a post 
date: 2020-01-21
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Attributes

- An Attribute directive changes the appearance or behavior of a DOM element.

- Most common attributes
  -   NgClass—adds and removes a set of CSS classes.
  -   NgStyle—adds and removes a set of HTML styles.
  -   NgModel—adds two-way data binding to an HTML form element.


##### Task 1: Binding to Class - ngClass, class

```html
<div [ngClass]="isSpecial ? 'special' : ''">This div is special</div>
```


Note :

- To add or remove a single class, use class binding rather than NgClass.

```html
<div [class.special]="isSpecial">This div is special</div>
```


###### Binding to styles

```html
    [style.width]="100px"
    [style.width.px]="100"
    [style]="expression"
```


###### Task 2: Disable form submit button if form is invalid
```html
   <form #f="ngForm">
        <input type="text" name="username" ngModel>
        <button [disabled]="f.invalid">Submit</button>
   </form>
```

