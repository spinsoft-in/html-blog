---
title: Form -2
description: 
date: 2022-11-03
day: 3.2
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Form -1

* tasks/new

```tsx
    "use client";

    import { useState } from "react";
    import toast from "react-hot-toast";

    export default function AddTask() {

        const [isLoading, setIsLoading] = useState<boolean>(false)
        const [error, setError] = useState<string | null>(null)

        const handleSubmit = async (event:any) => {
            event.preventDefault();
            setIsLoading(true);
            setError(null) // Clear previous errors when a new request starts

            // Extract the form values
            try{
                const name = event.target.name.value;

                //validate form fields
                if(name != null && name.trim() === "") {
                    throw new Error("Task name cannot be empty");
                }
                
                const data = {
                    name: name
                };
                
                // Convert the data to JSON format
                const taskObj = JSON.stringify(data);
                toast.success(taskObj);
                toast.success('Form Submitted');
            }catch(error:any){
                // Capture the error message to display to the user
                setError(error.message);
                console.error(error);
                toast.error(error.message);
            } finally {
                setIsLoading(false)
            }
        };

        return (
            <main>
            <h3>Add Task</h3>
            {error && <div style={{ color: 'red' }}>{error}</div>}
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