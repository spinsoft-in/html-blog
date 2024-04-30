---
title: class
description: 
date: 2020-01-26
duration: ~30 mins
tags:
layout: layouts/post.njk
---

###### Task 1: Create model class for User

```ts
export interface User {
  id: number;
  name: string;
  gender?: string;
  email: string;
  password:string
}
```