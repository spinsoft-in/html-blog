---
title: Route Navigation
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Create Navigation

### Declare Router

* Import router in navigation
```tsx
    import { useRouter } from "next/navigation";
    const router = useRouter();
    router.push("/login");
```

### Task 1: Create a button which should navigate to Login page

```tsx
    "use client";
    import { useRouter } from "next/navigation";
    import toast from "react-hot-toast";

    export default function Home() {

        const router = useRouter();

        return (
            <main>
                <h3>Welcome to TodoApp</h3>
                
                <button onClick={()=>{
                    router.push("/login");
                }
                }> Go to Login Page</button>
            </main>
        );
    }
```

