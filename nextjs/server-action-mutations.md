---
title: Server Actions and Mutations
description: 
date: 2022-11-03
day: 10
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Server Actions and Mutations

* Server Actions are asynchronous functions that are executed on the server. 
* They can be used in Server and Client Components to handle form submissions and data mutations in Next.js applications.

A Server Action can be defined with the React "use server" directive. You can place the directive at the top of an async function to mark the function as a Server Action, or at the top of a separate file to mark all exports of that file as Server Actions.


#### Server Components

* Server Components can use the inline function level or module level "use server" directive. 
* To inline a Server Action, add "use server" to the top of the function body:

```tsx
    // Server Component
    export default function Page() {
        // Server Action
        async function create() {
            'use server'
        
            // ...
        }
        
        return (
            // ...
        )
    }
```

#### Client Components

* Client Components can only import actions that use the module-level "use server" directive.

* To call a Server Action in a Client Component, create a new file and add the "use server" directive at the top of it. All functions within the file will be marked as Server Actions that can be reused in both Client and Server Components:

* `app/actions.ts`
```tsx
    'use server'
    
    export async function create() {
        // ...
    }
```



* `app/ui/button.tsx`
```tsx
    import { create } from '@/app/actions'
    
    export function Button() {
        return (
            // ...
        )
    }
```


You can also pass a Server Action to a Client Component as a prop:

```tsx
    <ClientComponent updateItem={updateItem} />
```

```tsx
    'use client'
    
    export default function ClientComponent({ updateItem }) {
        return <form action={updateItem}>{/* ... */}</form>
    }
```