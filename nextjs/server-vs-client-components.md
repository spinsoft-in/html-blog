---
title: Server vs Client Components
description: 
date: 2022-11-03
day: 3
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

### Server and Client Components

* When building React applications, you will need to consider what parts of your application should be rendered on the server or the client. This page covers some recommended composition patterns when using Server and Client Components.

### When to use Server and Client Components?

* Here's a quick summary of the different use cases for Server and Client Components:

|Sno| Scenario | Server Component | Client Component |
|--|--|--|--|
|1|Fetch data		|  Y |  |
|2|Access backend resources (directly)|  Y |  |
|3|Keep sensitive information on the server (access tokens, API keys, etc)		|  Y |  |
|4|Keep large dependencies on the server / Reduce client-side JavaScript		| Y |  |
|5|Add interactivity and event listeners (onClick(), onChange(), etc)		|  | Y |
|6|Use State and Lifecycle Effects (useState(), useReducer(), useEffect(), etc)	|  | Y |
|7|Use browser-only APIs		|  | Y |
|8|Use custom hooks that depend on state, effects, or browser-only APIs	|  | Y |
|9|Use React Class components		|  | Y |
