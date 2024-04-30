---
title: Client Side Data Fetching using useEffect
description: 
date: 2022-11-03
day: 5
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Client Side Data Fetching using useEffect


```tsx
  import { useState, useEffect } from 'react'
  
  function Profile() {
    const [data, setData] = useState(null)
    const [isLoading, setLoading] = useState(true)
  
    useEffect(() => {
      fetch('/api/profile-data')
        .then((res) => res.json())
        .then((data) => {
          setData(data)
          setLoading(false)
        })
    }, [])
  
    if (isLoading) return <p>Loading...</p>
    if (!data) return <p>No profile data</p>
  
    return (
      <div>
        <h1>{data.name}</h1>
        <p>{data.bio}</p>
      </div>
    )
  }
  ```