---
title: Environment Variables
description: This is a post 
date: 2020-04-10
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Dev Environment - environment.ts

```ts
    export const environment = {
        production: false,
        API_URL : "http://localhost:5000/api"
    };
```

###### Production Environment - environment.prod.ts

```ts
    export const environment = {
        production: true,
        API_URL : "http:/your project-mock-api.herokuapp.com/api"
    };
```

###### Use environment Variable

```ts
    import { environment } from '../../environments/environment';

    @Injectable({
        providedIn: 'root'
    })
    export class AuthService {

        private apiUrl:string ;
        constructor() { 
            this.apiUrl =  environment.API_URL;
            console.log(this.apiUrl);
        }
    }
```