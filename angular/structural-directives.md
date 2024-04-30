---
title: Structural Directives
description: This is a post 
date: 2020-01-20
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: *ngIf - Directives

- This menu link "View Balance" should be displayed, only if the user is loggedin

```html
   <a class="nav-link" routerLink="viewBalance"> View Balance </a>
```

###### Task 2: Component TS file and Template HTML file

```ts
    isLoggedIn =  localStorage.getItem("LOGGED_IN_USER") != null ? true: false;
```

###### Task 2.1: Hide Element ( Approach -1 )

```html
    <a routerLink="viewBalance" [class.hidden]="!isLoggedIn"> View Balance </a>
```

```html
   <a routerLink="viewBalance" *ngIf="isLoggedIn"> View Balance </a>
```

###### Differences between Hide and NgIf

- When you hide an element, that element and all of its descendants remain in the DOM. All components for those elements stay in memory and Angular may continue to check for changes. You could be holding onto considerable computing resources and degrading performance unnecessarily.


- NgIf works differently. When NgIf is false, Angular removes the element and its descendants from the DOM. It destroys their components, freeing up resources, which results in a better user experience.

- If you are hiding large component trees, consider NgIf as a more efficient alternative to showing/hiding.


###### Task : Iterate array and display

```ts
    departments = ["CSE","IT","EEE"];
```

```html
    <div *ngFor="let dept of departments">{{dept}}</div>
```

###### Task : Iterate with index

```html
    <div *ngFor="let dept of departments;let i=index">    
    {{i+1}} - {{dept}}
    </div>
```


###### Task : Switch Case

```html
    <div [ngSwitch]="currentItem.feature">
    <app-stout-item    *ngSwitchCase="'stout'"    [item]="currentItem"></app-stout-item>
    <app-device-item   *ngSwitchCase="'slim'"     [item]="currentItem"></app-device-item>
    <app-lost-item     *ngSwitchCase="'vintage'"  [item]="currentItem"></app-lost-item>
    <app-best-item     *ngSwitchCase="'bright'"   [item]="currentItem"></app-best-item>
    <!-- . . . -->
    <app-unknown-item  *ngSwitchDefault           [item]="currentItem"></app-unknown-item>
    </div>
```