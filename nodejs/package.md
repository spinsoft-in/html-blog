---
title: Package Configuration
description: 
date: 2020-01-03
duration: ~10 mins
layout: layouts/post.njk
---


### package.json
  
```json
  {
    "name": "demo-project",
    "version": "1.2.3",
    "description": "Demo Project",
    "main": "server.js",
    "scripts": {
      "start": "node server.js"
    },
    "keywords": [],
    "author": "",
    "license": "ISC",
  
  }

```

#### Task 1: Package Details

```js
  "name": "demo-project",
  "version": "1.0.0",
  "description": "Demo Project",
```

### Task 2: Versioning

- Format: major.minor.patch
- major release, minor release, patch release
- Reference: https://docs.npmjs.com/about-semantic-versioning
  
```js
    "version": "1.2.3",
```

* Major Version : 1
* Minor Version : 2
* Patch Version : 3

###### Task 3: Dependencies

- "dependencies": Packages required by your application in production.

```js
  "dependencies": {
    "bootstrap": "^4.5.3",
    "http-server": "^0.12.3",
    "jquery": "^3.5.1",
    "lodash": "^4.17.20"
  },
```

#### Task 4: Development Dependencies
- "devDependencies": Packages that are only needed for local development and testing.


```js
 "devDependencies": {
      "html-webpack-plugin": "^5.0.0-alpha.14",
      "webpack": "^5.4.0",
      "webpack-cli": "^4.2.0"
    }
```