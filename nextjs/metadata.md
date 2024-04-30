---
title: Metadata and Favicon
description: 
date: 2022-11-03
day: 2
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---


## Metadata and Favicon

#### Task 1: Edit Metadata

* Edit `layout.tsx`

```tsx
    export const metadata: Metadata = {
        title: "TodoApp",
        description: "Task Management App",
    };

```

#### Task 2: Add Favicon in head

* Add favicon in `public` folder

* Edit `layout.tsx` and add `head` section

```tsx
    import favicon from "../../public/favicon.ico";


    <head>
        <link rel="shortcut icon" type="image/x-icon" href={favicon.src} />
    </head>

```

