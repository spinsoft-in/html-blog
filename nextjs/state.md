---
title: useState
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---


### useState

```tsx
    import { useState } from "react";
    const [count, setCount] = useState(0);
```

### Action

```tsx
    <button onClick={() => setCount(count + 1)}>Click me</button>
```

### Task 1: Create a Counter program which increases the count value


```tsx
    "use client";

    import { useState } from "react";

    export default function Counter() {

        const [count, setCount] = useState(0);
        return (
            <main>
                <p>You clicked {count} times</p>
                <button onClick={() => setCount(count + 1)}>Click me</button>
            </main>
        );
    }
```

