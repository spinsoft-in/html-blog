---
title: Template Driven Forms
description: 
date: 2020-11-05
duration: ~30 mins
tags:
layout: layouts/post.njk
---


###### Prerequisite: Create login form ( Plain HTML/JS)

```html
    <form onsubmit="login()">
        <input type="email" name="email" required placeholder="Enter Email" autofocus> 
        <input type="password" name="password" required placeholder="Enter Password" > 
        <button>Submit</button>
    </form>
```


###### Task 1: Import FormsModule

``` js
  imports:[
      ...
      FormsModule
  ]
```


###### Task 2.1: Create login form and use Angular Form Tags (ngForm,ngModel,ngFormGroup)

```html
    <form (ngSubmit)="login(loginForm)" #loginForm="ngForm">
        <input type="email" name="email" ngModel required placeholder="Enter Email" autofocus> 
        <input type="password" name="password" ngModel required placeholder="Enter Password" > 
        <button>Submit</button>
    </form>
```

```js
    login(form:NgForm){
        console.log(form);
        let formData = form.value;
        console.log(formData);
        console.log("Email", formData.email);
        
    }
```


###### Task 2.2: Call login method on submit ( Event Binding)
```html
    <form #loginForm="ngForm" (ngSubmit)="login(loginForm)">
    <button [disabled]="loginForm.invalid">Submit</button>
```

###### Task 2.3: Disable Submit Button if formData is invalid ( Attribute Binding)
```html
    <form #loginForm="ngForm" (ngSubmit)="login(loginForm)">
    <button [disabled]="loginForm.invalid">Submit</button>
    </form>
```


###### Task 3: Create login form with Model Attributes ( two way data binding)

```html
    <form (ngSubmit)="login(loginForm)" #loginForm="ngForm">
        <input type="email" name="email" [(ngModel)]="email" required placeholder="Enter Email" autofocus> 
        <input type="password" name="password" [(ngModel)]="password" required placeholder="Enter Password" >
        <button>Submit</button>
    </form>
```

```js
    email:string;
    password:string;

    login(form:NgForm){
        console.log("Email:" , this.email);
        console.log("Password:" , this.password);
        //check login credentials
    }

```

###### Task 4: Clear Form Data

```js
    login(form:NgForm){
        form.reset();
    }
```