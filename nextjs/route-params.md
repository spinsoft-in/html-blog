---
title: Route Params
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Route Params

* The `useParams` hook is one of the several hooks in React router.
* You can use it to retrieve route parameters from the component rendered by the matching route.


* Import `useParams` in navigation

```tsx
    import { useParams } from "next/navigation";
    const { id } = useParams<{ id: string }>();
```

### Task 1: Create ViewTask Page 

* http://localhost:3000/tasks/101

* Create page - `tasks/[id]/page.tsx`

```tsx
    "use client";

    import { useParams } from "next/navigation";

    export default function ViewTask() {

        const { id } = useParams<{ id: string }>();
        console.log("id:", id);
        return (
            <main>
                Task Id : {id}
            </main>
        );
    }



```

