---
title: Custom Directives
description: This is a post 
date: 2020-01-11
duration: ~20 mins
sections: Task 1
tags:
layout: layouts/post.njk
---

###### Task 1: Create Directive - highlight

```js
  ng g directive highlight
```


###### Task 2: Implement highlight directive logic.

- highlight.directive.ts
  

```ts
    import { Directive } from '@angular/core';

    @Directive({
    selector: '[appHighlight]'
    })
    export class HighlightDirective {
      constructor(el: ElementRef) {
       el.nativeElement.style.backgroundColor = 'yellow';
      }
    }
```

```html
    <p appHighlight>Highlight me!</p>
```
