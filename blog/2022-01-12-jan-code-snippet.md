---
title: January Code Snippet
path: /jan-code-snippet
date: 2022-01-12
summary: Random code snippets to help you get started on your next project
tags: ['coding', 'frontend']
---

![background](./images/blog_bg_6.jpg)

The purpose of this article is to post random code snippets that I find. I know that it can be useful to someone else other than me in some way. My thinking is to start posting one or two a month. If things go well then I will gladly post more as I find them or think of them. I'm not one to claim that I know all there is about the web and how to best set up your web projects. There will always be more than one way to do the same thing. The code snippet for this article will be using CSS variables. If you don't know anything about CSS variables you can read about them [here](https://www.w3schools.com/css/css3_variables.asp). 

This code will make it so that you only have to define your font size one time and the browser will calculate the best size to display according screen size. 

```CSS
:root {
  --base-size: 1em;
  --type-scale: 1.2;
  --h5: calc(var(--base-size) * var(--type-scale));
  --h4: calc(var(--h5) * var(--type-scale));
  --h3: calc(var(--h4) * var(--type-scale));
  --h2: calc(var(--h3) * var(--type-scale));
  --h1: calc(var(--h2) * var(--type-scale));
}

h1 { 
  font-size: var(--h1);
}

h2 {
  font-size: var(--h2);
}

h3 {
  font-size: var(--h3);
}

h4 {
  font-size: var(--h4);
}

h5 {
  font-size: var(--h5)
}
```


