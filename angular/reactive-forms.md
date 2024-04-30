---
title: Reactive Forms
description: 
date: 2020-11-06
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


###### Task 1: Import ReactiveFormsModule

``` js
  imports:[
      ...
      FormsModule,
      ReactiveFormsModule
  ]
```

###### Task 2: Create login form with Reactive Forms

```html
    <form (ngSubmit)="login()" #loginForm="ngForm" formGroup="loginFormGroup">
    <input type="email" name="email" formControlName="email" required placeholder="Enter Email" autofocus> 
    <input type="password" name="password" formControlName="password" required placeholder="Enter Password" >
    <button>Submit</button>
    </form>
```

```js
    loginFormGroup = new FormGroup({
        email: new FormControl(''),
        password: new FormControl('')
    });

    login(){
        console.log(this.loginFormGroup.value);
        console.log("Email:" , this.loginFormGroup.controls['email'].value);
        console.log("Password:" , this.loginFormGroup.value.password);
    }

```

###### Task 3: Add Validations to login fields

```js
    loginFormGroup = new FormGroup({
        email: new FormControl('', Validators.required),
        password: new FormControl('', [Validators.required, Validators.minLength(8)])
    });
```

###### Task 4: Implement FormBuilder

```js
    constructor(private fb:FormBuilder){ }

    loginFormGroup = this.fb.group({
        email: '',
        password: ''
    });
```