---
title: Form -1
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Form -1

* tasks/new

```tsx
    "use client";

    export default function AddTask() {

        return (
            <main>
            <h3>Add Task Form</h3>
            </main>
        );
    }


```

#### Task 1: Add a Task 

```tsx
    "use client";

    export default function AddTask() {

        const handleSubmit = (event:any) => {
            event.preventDefault(); // Prevent the default form submission behavior
            alert("Form Submitted");

        };

        return (
            <main>
            <h3>Add Task</h3>
            <form onSubmit={handleSubmit}>
                <div>  
                    <label htmlFor="name">Task Name:</label>
                    <input type="text" name="name" id="name" required placeholder="Enter task name"/>
                </div>
                <div>
                    <button type="submit">Submit</button>
                </div>
            </form>
            </main>
        );
    }


```


### Task 2: Add formSubmission State and add toastr message

```tsx
    import { useState } from "react";
    import toast from "react-hot-toast";

    const [formSuccess, setFormSuccess] = useState(false)

    const handleSubmit = (event:any) => {
        event.preventDefault();
        // alert("Form Submitted");
        setFormSuccess(true);
        toast.success('Form Submitted');
    };

```

#### Task 3: Form submission without JS

```tsx
    <form action="/api/tasks" method="post">
```

#### Task 4: Get form data

```tsx

    // Extract the values of the "name" and "email" inputs from the form
    const data = {
        name: event.target.name.value
    };

    // Convert the data to JSON format
    const taskObj = JSON.stringify(data);
    toast.success(taskObj);
```