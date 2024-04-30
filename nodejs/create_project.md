---
title: Create Node JS Project using NPM
description: 
date: 2020-01-02
duration: ~10 mins
tags:
layout: layouts/post.njk
---

### Task 1:  Create Node JS Project

```js
  mkdir project1
  cd project1
```

### Task 2: Initialize Node JS Project

```js
  npm init
```

Note: Press Enter to use the default values.

```bash
  package name: (project1)
  version: (1.0.0)
  description:
  entry point: (index.js)
  test command:
  git repository:
  keywords:
  author:
  license: (ISC)
  About to write to D:\Sify\nodejs\project1\package.json:

  {
    "name": "project1",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC"
  }


  Is this OK? (yes)
```
(or)

### Task 3: Open the package.json

```js
  {
    "name": "project1",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC"
  }

```

### Task 4: Create a second project 


```js
    mkdir project2
    cd project2
    npm init -y
```
