---
title: Create Project
description: 
date: 2022-11-03
day: 1
duration: ~10 mins
tags:
  - nextjs
layout: layouts/post.njk
---

## Create Project

#### Task 1: Create a project `todoapp`

```bash
    C:\projects>npx create-next-app@latest
    Need to install the following packages:
    create-next-app@14.2.2
    Ok to proceed? (y) y
```

* Typescript: Yes
* ESLint: No
* Tailwind CSS: No
* src: Yes
* App Router: Yes
* Customize Alias : No

```bash  
    √ What is your project named? ... todoapp
    √ Would you like to use TypeScript? ... No / Yes
    √ Would you like to use ESLint? ... No / Yes
    √ Would you like to use Tailwind CSS? ... No / Yes
    √ Would you like to use `src/` directory? ... No / Yes
    √ Would you like to use App Router? (recommended) ... No / Yes
    √ Would you like to customize the default import alias (@/*)? ... No / Yes
    Creating a new Next.js app in C:\Users\Naresh\Downloads\todoapp.

    Using npm.

    Initializing project with template: app


    Installing dependencies:
    - react
    - react-dom
    - next

    Installing devDependencies:
    - typescript
    - @types/node
    - @types/react
    - @types/react-dom

    added 28 packages, and audited 29 packages in 36s

    3 packages are looking for funding
    run `npm fund` for details

    found 0 vulnerabilities
    Initialized a git repository.

    Success! Created todoapp at C:\projects\todoapp
```

#### Task 2: Go to the project directory


```bash
    cd todoapp
```

#### Task 3: Open the project in VSCode

```bash
    code .
```

#### Task 4: Run the project

```bash
    npm run dev
```

```bash
    > todoapp@0.1.0 dev
    > next dev

    ▲ Next.js 14.2.2
    - Local:        http://localhost:3000

    ✓ Starting...
    ✓ Ready in 3.4s
```

#### Task 5: Test the URL

* http://localhost:3000/


#### Task 6: Remove the default page styles and contents

* globals.css ( Remove all css contents)
* page.module.css ( Remove all css contents )
* page.tsx ( Remove all html contents and add your content)

```tsx
    export default function Home() {
        return (
            <main>
            <h3>Welcome to TodoApp</h3>
            </main>
        );
    }

```