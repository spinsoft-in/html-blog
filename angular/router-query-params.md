---
title: Routing - Query Params
description: This is a post 
date: 2020-02-02
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: Search By Category - Query Params

- http://localhost:4200/products?category=ALL

```html
    <a (click)="gotoProducts()">All Products</a>
```

```ts
    gotoProducts() {
        this.router.navigate(['/products'], { queryParams: { category: 'ALL' } });
}
```

``` js
   routes = [
       {path:'products', component:ListProductComponent}
   ];
```


###### Task 2: Get Category from Query Params (i.e category=ALL)

``` js
  category:string;
  constructor(private route:ActivatedRoute) { 
      this.route.queryParams.subscribe(params=>{
          this.category = params["category"];
          console.log("Category:" + this.category);
      });
  }
  

```

###### Task 3: Test Router Query Params

- http://localhost:4200/products?category=ALL
