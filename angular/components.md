---
title: Components
description: 
date: 2020-01-15
duration: ~30 mins
tags:
layout: layouts/post.njk
---


###### What is Component in Angular  ?

Components are the main building block for Angular applications. Each component consists of:

- An HTML template that declares what renders on the page
- A Typescript class that defines behavior
- CSS selector that defines how the component is used in a template
- Optionally, CSS styles applied to the template


```ts
    @Component({
        selector: 'app-root',
        templateUrl: './app.component.html',
        styleUrls: ['./app.component.css']
    })
    export class AppComponent {
    
    }
```


######  Create Component

```js
    ng generate component components/login
```

By default, this command creates the following:

- A folder named after the component
- A component file, <component-name>.component.ts
- A template file, <component-name>.component.html
- A CSS file, <component-name>.component.css
- A testing specification file, <component-name>.component.spec.ts


###### Component Decorator

```js
    @Component({

    })
```