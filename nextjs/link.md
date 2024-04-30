---
title: Link
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Create Link

### Declare Router

* Import router in navigation
```tsx
    import Link from "next/link";
    <Link href={`/login`}>Login</Link>
```

### Task 1: Create a Link 

* Create a Link which should navigate to Login page

```tsx
    "use client";
    import Link from "next/link";

    export default function Home() {

        return (
            <main>
                <Link href={`/login`}>Login</Link>
            </main>
        );
    }

```

