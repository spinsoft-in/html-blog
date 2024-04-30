---
title: Lifecycle Methods  - init,destroy
description: This is a post 
date: 2020-01-10
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: Implement OnInit,OnDestroy

- Constructor will get called before OnInit
- OnInit, OnDestroy will get called only once.

```js
  export class AppComponent implements OnInit,OnDestroy{
  
        constructor(){
            console.log("Constructor")
        }
        ngOnInit(): void {
            console.log("OnInit");
        }
        ngOnDestroy(): void {
            console.log("OnDestroy");
        }

    }
```

