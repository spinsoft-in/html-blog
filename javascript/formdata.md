---
title: Access Form Data
description: This is a post on My Blog about agile frameworks.
date: 2020-01-10
duration: ~30 mins
layout: layouts/post.njk
---

###### Prerequisite 1: Design an HTML Form

```html
    <h3>Registration Form</h3>
   <form id="regForm" onsubmit="register()">
   Name: <input type="text" id="name"  />  <br/>
   DOB: <input type="date" id="dob" placeholder="Date of Birth"/> <br/>
   Role:
   <select id="role">
        <option value="" disabled> -- SELECT -- </option>
        <option value="U"> USER </option>
        <option value="A"> ADMIN </option>
    </select>
    <br/>   
   Gender: <input type="radio" name="gender" value="M"> Male 
   <input type="radio" name="gender" value="F"> Female <br/>
   
    Interested Technologies: 
    <input type="checkbox" name="technologies" value="js"> JavaScript 
    <input type="checkbox" name="technologies" value="angular"> Angular 
    <input type="checkbox" name="technologies" value="html"> HTML
    <br/>
    <button>Submit</button> 
   </form>
```

###### Prerequisite 2: Create a JavaScript function with an alert message and test it.
```js
<script>
    function register(){
        event.preventDefault();
        alert("Register button clicked");
        // Need to add code here
    }
</script>
```


###### Task 1: Get Name field value

```js
    let name = document.getElementById("name").value;
    console.log(name);
```

###### Task 2: Get Date of birth field value

```js
    let dob = document.getElementById("dob").value; 
    // input type="date" returns date in "yyyy-MM-dd" format
    console.log(dob);
```

###### Task 3: Get Role option value

```js
    let role = document.getElementById("role").value; 
    console.log(role);
```

###### Task 4: Get Gender radio button value 

```js
    let genderOptions = document.getElementsByName("gender");
    console.log(genderOptions); //It will return array.
    //iterate array
    let gender = null;
    for(let option of genderOptions){
        if (option.checked){
            gender = option.value;
            break; // we can select only one value in radio button
        }
    }
    console.log("Selected Gender:" , gender);
```

##### Task 5: Get Technologies checkbox value 

```js
    let technologiesOptions = document.getElementsByName("technologies");
    let technologies= [];
    for(let option of technologiesOptions){
        if(option.checked){
            technologies.push(option.value);
        }
    }
    console.log("Selected Technologies", technologies);
```

##### Task 6: Store all the data in a single object

```js
    let user = { name: name, dob: dob, role:role, gender:gender, technologies: technologies };
    console.log(user);
    alert("Successfully Registered");
```

##### Task 7: After successful registration, clear the form data

```js
    let regForm = document.getElementById("regForm"); //<form id="regForm"> 
    regForm.reset();
```