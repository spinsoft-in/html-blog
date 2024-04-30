---
title: Routing - Path Variables
description: This is a post 
date: 2020-02-02
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: Search By Category - Path Variables

- http://localhost:4200/products/ALL

```html
    <a routerLink="products/ALL">All Products</a>
    <a routerLink="products/MOBILE">Mobile</a>
    <a routerLink="products/LAPTOP">Laptop</a>
```

``` js
   routes = [
       {path:'products/:category', component:ListProductComponent},
       {path:'viewproduct/:id', component:ViewProductComponent}

   ];
```

- Note the path variable syntax ( :category)

###### Task 2: Get Category from Path Params (i.e category=ALL)

``` js
  category:string;
  constructor(private route:ActivatedRoute) { 
      this.route.params.subscribe(params=>{
          this.category = params["category"];
          console.log("Category:" + this.category);
      });
  }
  

```

###### Task 3: Test Router - with different Path Variables

- http://localhost:4200/products/ALL
- http://localhost:4200/products/MOBILE
