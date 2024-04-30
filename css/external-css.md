---
title: External CSS
description: 
date: 2020-11-03
duration: ~10 mins
day: 1
tags:
  - css
layout: layouts/post.njk
---

## External Stylesheet

* An external CSS stylesheet can be applied to any number of HTML documents by placing a `<link>` element in each
HTML document.

```html
    <link rel="stylesheet" type="text/css" href="style.css">
```

* The attribute rel of the `<link>` tag has to be set to "stylesheet"
* The `href` attribute to the relative or absolute path to the stylesheet. 
* While using relative URL paths is generally considered good practice, absolute paths can be used, too. 
* In HTML5 the `type` attribute can be omitted.


```html
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8" />
        <link rel="stylesheet" type="text/css" href="style.css">
    </head>
    <body>
        <h1>Hello world!</h1>
    </body>
    </html>
```

* `style.css`

```css
    h1 {
        color: green;
    }
```

* **Reference**: CSSNotesForProfessionals.pdf - Section 1.1
