---
title: "Underscore: each"
date: 2019-05-15
tags: ["Algorithm", "자바스크립트"]
url: https://sub2n.github.io/2019/05/15/Underscore-each/
---

# Underscore: each

![each pass](https://user-images.githubusercontent.com/48080762/57747874-59ba2980-7712-11e9-8a09-b7f1825254e4.png)

```js
_.each = function(collection, iterator) {
  if (Array.isArray(collection)) {
    for (let index = 0; index < collection.length; index++) {
      iterator(collection[index], Number(index), collection);
    } 
  } else {
    for (let key in collection) {
      if (key !== 'someProperty')
        iterator(collection[key], key, collection);
    }   
  } 
};
```