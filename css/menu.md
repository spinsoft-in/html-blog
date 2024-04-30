---
title: Menu
description: 
date: 2020-11-03
duration: ~10 mins
day: 2
tags:
  - css
layout: layouts/post.njk
---

#### Create Menu

* **Chatgpt**: create menu using html ul li tag.

* Create a simple horizontal menu with four items: Home, About, Services, and Contact.

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Menu Example</title>
      <style>
          /* Basic styling for the menu */
          ul {
              list-style-type: none;
              margin: 0;
              padding: 0;
          }
          li {
              display: inline;
              margin-right: 10px;
          }
          a {
              text-decoration: none;
              color: #333;
              font-weight: bold;
          }
          a:hover {
              color: #666;
          }
      </style>
  </head>
  <body>
      <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Services</a></li>
          <li><a href="#">Contact</a></li>
      </ul>
  </body>
  </html>
```