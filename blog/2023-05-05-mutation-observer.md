---
title: Let's talk about the MutationObserver in JavaScript 
path: /mutation-observer-in-javascript
date: 2023-05-05
summary: The MutationObserver is a powerful tool that allows us to observe changes to the DOM in real time. This post will cover the basics of using the MutationObserver, as well as some common use cases for it.
tags: ['coding', 'frontend', 'javascript', 'mutation-observer']
---

![background](./images/blog_bg_7.jpg)

As web developers, we are always looking for ways to improve the user experience of our web applications. One way we can do this is by using the MutationObserver in JavaScript. The MutationObserver is a powerful tool that allows us to observe changes to the DOM (Document Object Model) in real time.

In this post, we'll cover the basics of using the MutationObserver, including what it is, how to set it up, and some use cases.

## What is the MutationObserver?

The MutationObserver is a built-in JavaScript API that allows us to observe changes to the DOM. It works by watching for changes to a particular node or a group of nodes and notifying us when those changes occur.

The MutationObserver can detect changes such as:
   - Adding or removing elements from the DOM
   - Changing attirbutes of elements
   - Changing the text content of elements
   - Moving elements around in the DOM

## Setting up the MutationObserver

To set up the MutationObserver, we need to create a new instance of it and pass in a callback function. This callback function will be called whenever a change is detected in the DOM.

```js
const observer = new MutationObserver((mutations) => {
  // Do something with the mutations
});
```   

This code creates a new instance of the MutationObserver and passes in a callback function. The callback function will be called whenever a change is detected in the DOM. The 'mutations' parameter is an array of MutationRecords, which contain information about the changes that occurred.

To start observering changes to a particualar node, we can use the 'observe' method of the of the observer instance. Here's an example:

```js 
const targetNode = document.getElementById('target');
const config = { attributes: true, childList: true, subtree: true };

observer.observe(targetNode, config);
```

In this example, we are observing changes to the 'targetNode' element. The 'config' object specifies which types of changes we want to observe. In this case, we are observing changes to the attributes, child nodes, and subtree of the target node.

## Use cases for the MutationObserver

Now that we know show to set up MutationObserver, let's look at some use cases for it.

## Lazy loading images

Lazy loading images is a technique used to defer loading of non-critical resources such as images until they are needed. This can improve the performance of a web page by reducing the amount of data that needs to be downloaded. By using the MutationObserver, we can detect when an image enters the viewport and trigger its loading.

```js
const observer = new MutationObserver((mutations) => {
  mutations.forEach((mutation) => {
    if (mutation.type === 'childList') {
      mutation.addedNodes.forEach((node) => {
        if (node.tagName === 'IMG') {
          const img = node;
          const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
              if (entry.isIntersecting) {
                img.src = img.dataset.src;
                observer.unobserve(img);
              }
            });
          });
          observer.observe(img);
        }
      });
    }
  });
});

observer.observe(document.body, { childList: true, subtree: true });
```
In this example, we are using the MutationObserver to watch for changes to the DOM and detect when an 'img' element is added. We then create a new 'IntersectionObserver' instance and observe the 'img' element. When the 'img' element enters the viewport, we set its 'src' attribute. This triggers the browser to load the image.

As you can see, the MutationObserver is a powerful tool that can be used to improve the user experience of your web applications. It allows you to observe changes to the DOM in real time and react accordingly. I hope this post has given you some ideas on how to use the MutationObserver in your own projects. Thanks for reading!
