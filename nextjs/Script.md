---
title: Script
description: 
date: 2022-11-03
day: 4
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Script

```tsx
  import Script from 'next/script'

  export default function Dashboard() {
    return (
      <>
        <Script src="https://example.com/script.js" />
      </>
    )
  }
```