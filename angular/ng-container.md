---
title: ng-container
description: 
date: 2020-01-25
duration: ~30 mins
tags:
layout: layouts/post.njk
---

###### Prerequisite: 

```ts
    loggedInUser = { id :1, name:"Naresh", role:"ADMIN"}
```

###### Task 1: Display a link if the loggedInUser is "ADMIN"

```html
    <a *ngIf="loggedInUser=='ADMIN'">Welcome {{loggedInUser.name}} </a>
```

###### Task 2: Display the loggedInUser role

```html
    <p>
        Welcome {{loggedInUser.name}} 
  <ng-container *ngIf="loggedInUser">
    ( {{loggedInUser.role}} )
  </ng-container>
    </p>
  ```

###### Task 3: Display Roles

```js
    roles = ["USER","ADMIN", "TRAINER","MANAGER"];
```

```html
    <p> Roles - 
     <ng-container *ngFor="let role of roles; let first=first; let last=last">
      <ng-container *ngIf="!first">,</ng-container>
      <ng-container *ngIf="last">and</ng-container>
      {{role}}
    </ng-container>.
    </p>
```
