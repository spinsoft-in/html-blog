---
title: DatePipe
description: This is a post 
date: 2020-01-26
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

##### Date Pipe

- Reference: https://angular.io/api/common/DatePipe

###### Task 1:  Create createdDate

- app.component.ts
  
```ts
    createdDate =  new Date().toJSON();//
```

- app.component.html
  
```ts
    {{createdDate}}
```

##### Task 2: Format the Date

```js
    {{ createdDate | date }}        // output is 'Jun 15, 2015'
    {{ createdDate | date:'medium' }}      // output is 'Jun 15, 2015, 9:43:11 PM'
    {{ createdDate | date:'shortTime' }}   // output is '9:43 PM'
    {{ createdDate | date:'mm:ss' }}       // output is '43:11'
    <p>The time is {{createdDate | date:'h:mm a z'}}</p>
```