---
title: Page Not Found
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

#### Create Page Not Found page

* Create File - `not-found.tsx`
```tsx
    import React from "react";

    const NotFound = () => {
        return (
            <div>
                Page Not Found
            </div>
            );
    };

    export default NotFound;

```

#### Test a invalid url

* http://localhost:3000/123

Note: It should display page not found page.