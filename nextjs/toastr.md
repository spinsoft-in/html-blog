---
title: Toastr
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Toastr

### Task 1 : Install Toastr

```bash
    npm install react-hot-toast
```

### Task 2: Include Toastr in Layout

```tsx
    import { Toaster } from "react-hot-toast";
    ...
    
    <body>
        <Toaster/>
        {children}
    </body>
```

* Create File - `not-found.tsx`
```tsx
    "use client";
    import toast from "react-hot-toast";

    export default function Home() {

    const notify = () => toast.success('Success');
    //const notify = () => toast.error('Failure');

    return (
        <main>
        <h3>Welcome to TodoApp</h3>
        <button onClick={notify}> Submit</button>
        </main>
    );
    }
        

```

#### Test a invalid url

* http://localhost:3000/123

Note: It should display page not found page.