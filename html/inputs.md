---
title: Input
description: 
date: 2020-11-03
duration: ~10 mins
tags:
  - HTML
layout: layouts/post.njk
---

#### Input Controls

###### Task 1: Label

```html
  <label for="username">Enter Username</label>
```

###### Task 2: Create Textbox

```html
  <input type="text" name="username" >
```

###### Task 2.1: Create Textbox with placeholder

```html
  <input type="text" name="username" placeholder="Enter Username" >
```

###### Task 2.2: Create Textbox with placeholder (Mandatory)

```html
  <input type="text" name="username" placeholder="Enter Username" required >
```

###### Task 2.3: Create Textbox with placeholder (Mandatory+Autofocus)

```html
  <input type="text" name="username" placeholder="Enter Username" required autofocus>
```

###### Task 2.3: Create Password Field

```html
  <input type="password" name="password" placeholder="Enter Password" required >
```

###### Task 2.4: Create a text box for Email Field

```html
  <input type="email" name="email" placeholder="Enter Email" required >
```

###### Task 2.5: Create a text box for age

```html
  <input type="number" name="age" placeholder="Enter Age" required >
```

###### Task 2.5.1: Create a text box for age with min and max

```html
  <input type="number" name="age" placeholder="Enter Age"  min="1" max="100" required >
```


###### Task 2.6: Create a text box for DateOfBirth

```html
  <input type="date" name="dob" placeholder="Enter Date of birth" required >
```

###### Task 2.6: Create a text box for Date (Restrict Dates)

```html
  <input type="date" name="dob" placeholder="Enter Date of birth" min="2020-01-01" max="2020-01-07" required >
```

###### Task 2.7: Create a radio button for gender

```html
  <input type="radio" name="gender" value="M" required > Male
  <input type="radio" name="gender" value="F" required > Female
```

###### Task 2.8: Create a checkbox for hobbies

```html
  <input type="checkbox" name="hobbies" value="M" required > Cricket
  <input type="checkbox" name="hobbies" value="F" required > Football
```

###### Task 2.9: Create a select for foodType(Veg/NonVeg)

```html
  <select name="foodtype">
    <option value="">--SELECT--</option>
    <option value="V">Veg</option>
    <option value="NV">NonVeg</option>
  </select>
```


###### Task 2.9.2: Create a select for state (default:VEG)

```html
  <select name="foodtype">
    <option value="">--SELECT--</option>
    <option value="V" selected>Veg</option>
    <option value="NV">NonVeg</option>
  </select>
```
