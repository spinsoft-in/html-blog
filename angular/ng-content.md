---
title: ng-content
description: 
date: 2020-01-26
duration: ~30 mins
tags:
layout: layouts/post.njk
---

###### Prerequisite: 

```ts
    loggedInUser = { id :1, name:"Naresh", role:"ADMIN"}
```

###### Task 1: Use ng-content for sidebar

```ts
    menus = [ {name:"Home", link:"home"},{name:"Dashboard", link:"dashboard"}];
```

```html
    <div class="sidebar">
        <ul>
        <li *ngFor="let m of menus"> <a routerLink="{{m.link}}"> {{m.name}} </a> </li>
            <ng-content></ng-content>
        </ul>
    </div>
```
