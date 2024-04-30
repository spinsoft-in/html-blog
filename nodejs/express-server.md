---
title: Express Static Server
description: 
date: 2020-02-15
duration: ~20 mins
layout: layouts/post.njk
---


###### Task 1: Install Express Server (mimimalist web framework)

- https://expressjs.com/
- https://www.npmjs.com/package/express ( ~15M weekly downloads)

```js
    npm i express
```

###### Task 2.1: Create app.js

```js
    const express = require('express')
    const app = express() 
    app.use('/static', express.static('public'))
    app.listen(3000)
```

###### Task 2.2: Create public folder and create index.html inside public folder

```html
    <html>
    <body>
        Static web pages
    </body>
    </html>
```

##### Task 2.3: Run the server

```js
    node app.js
```

###### Task 2.4: Test the server

- http://localhost:3000
