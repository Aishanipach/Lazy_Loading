# Infinite scroller♾️

Implementing infinite scroll and image lazy loading with the `HTML` `IntersectionObserver` API.

_Tasks pending:_
- Analyzing performance boost on lazy loading
- Further optimizing image content render


## The Intersection Observer API

According to the MDN docs, “the Intersection Observer API provides a way to asynchronously observe changes in the intersection of a target element with an ancestor element or with a top-level document's viewport”.

This allows us to implement functions such as infinite scroll and image lazy loading

The intersection observer is created by calling its constructor and passing it a callback and an options object. The callback is called whenever one element, called the `target`, intersects either the device viewport or a specified element (specified in the options argument).

`let observer = new IntersectionObserver(callback, options);`

The API is very easy to use. Let's see a typical example

```javascript
var intObserver = new IntersectionObserver(
  (entries) => {
    entries.forEach((entry) => {
      console.log(entry);
      console.log(entry.isIntersecting); // tells if the target intersects the root element
    });
  },
  {
    // default options
  }
);
let target = document.querySelector("#targetId");
intObserver.observe(target); // start observation
```

## Get started

1. Clone the repo
1. Run `yarn` to install the project dependencies
1. Run `yarn start` to start the project.
