---
title: NPM Dependency Install/Uninstall Commands
description: 
date: 2020-01-04
duration: ~20 mins
layout: layouts/post.njk
---

#### NPM Repository

- https://www.npmjs.com/

#### Prerequisite : Create a NodeJS Project

```js
  mkdir project1
  cd project1
  npm init -y
```

package.json

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
    "license": "ISC",
    "dependencies": {
      // Here all the dependencies will be added
    }
  }

```


#### Task 1: Install a Dependency Jquery

```js
  npm install jquery
```
(or)

```js
  npm i jquery
```

- In package.json, dependency entry added for jquery.

#### Task 1.1: Check node_modules folder for jquery.

- In node_modules/jquery folder, jquery files are downloaded.
  
```js
  "jquery": "^3.5.1",
```


#### Task 2: Uninstall a dependency

```js
  npm remove jquery
```



#### Task 3: Install multiple dependency in a single command

```js
  npm install jquery bootstrap
```

#### Task 4: Install bootstrap latest version

```js
  npm install bootstrap@latest
```

#### Task 5: Install bootstrap with a specific version

```js
  npm install bootstrap@3.3.6
```

