---
title: Http Server
description: 
date: 2020-02-10
duration: ~10 mins
layout: layouts/post.njk
---


###### Prerequisite : Install Http Server

- https://www.npmjs.com/package/http-server ( Weekly Downloads - 37M)
  
```js
    npm i http-server
```

###### Task 1: Create server.js file

- Http Server has a built-in http module.
- Reference : https://www.w3schools.com/nodejs/nodejs_http.asp

```js
    const http = require('http');
    // create Server
    http.createServer(function (request, response) {
        response.writeHead(200, {'Content-Type': 'text/plain'});
        response.end('Hello World');
    }).listen(8081);

    console.log('Server running at http://127.0.0.1:8081/');
```

###### Task 2: Start the server

```js
    node server.js
```

###### Task 3: Test the URL

- http://127.0.0.1:8081/
