---
title: Selectors
description: 
date: 2020-11-03
duration: ~10 mins
day: 2
tags:
  - css
layout: layouts/post.njk
---

### Basic Selectors

 CSS selectors identify specific HTML elements as targets for CSS styles. 


 |Selector |Description|
 |--|--|
 |*| Universal selector (all elements)|
 |div| Tag selector (all <div> elements)|
 |.blue| Class selector (all elements with class blue)|
 |.blue.red| All elements with class blue and red (a type of Compound selector)|
 |#headline| ID selector (the element with "id" attribute set to headline)|
 |:pseudo-class | All elements with pseudo-class|
 |::pseudo-element | Element that matches pseudo-element|
 |:lang(en) |Element that matches :lang declaration, for example `<span lang="en">`|
 |div > p |child selector|