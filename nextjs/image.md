---
title: Image
description: 
date: 2022-11-03
day: 4
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Image

```tsx
  import Image from 'next/image'
  
  export default function Page() {
    return (
      <Image
        src="/profile.png"
        width={500}
        height={500}
        alt="Picture of the author"
      />
    )
  }
```