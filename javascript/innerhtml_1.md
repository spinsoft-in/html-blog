---
title: InnerHTML - 1
description: This is a post on My Blog about agile frameworks.
date: 2020-01-10
duration: ~20 mins
layout: layouts/post.njk
---

###### Prerequisite 1: Design a HTML page with a div

```html
    <div id="message">
            Default Content
    </div>
```


##### Task 1: Display the content in the div in console
```js
    let messageDiv = document.querySelector("#message");
    console.log(messageDiv); // It will return "Default Content";
```

Note: Default content will be displayed.

###### Task 2: Update a new message in the div tag

```js
    messageDiv.innerHTML = "Successfully Registered";
```

###### Task 3: Insert a html content in the div block
```js
    messageDiv.innerHTML = "<font color='green'>Successfully Registered</font>";
```