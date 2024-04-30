---
title: Client Side Data Fetching using useSWR
description: 
date: 2022-11-03
day: 6
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Client Side Data Fetching using useSWR

* The team behind Next.js has created a React hook library for data fetching called SWR. 
* It is highly recommended if you are fetching data on the client-side. 
* It handles caching, revalidation, focus tracking, refetching on intervals, and more.

* Using use SWR to fetch the profile data. 
* SWR will automatically cache the data for us and will revalidate the data if it becomes stale.

```tsx
  import useSWR from 'swr'
  
  const fetcher = (...args) => fetch(...args).then((res) => res.json())
  
  function Profile() {
    const { data, error } = useSWR('/api/profile-data', fetcher)
  
    if (error) return <div>Failed to load</div>
    if (!data) return <div>Loading...</div>
  
    return (
      <div>
        <h1>{data.name}</h1>
        <p>{data.bio}</p>
      </div>
    )
  }
  ```