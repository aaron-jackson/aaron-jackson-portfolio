---
title: A Few Ways To Write Easier CSS
path: /a-few-ways-to-write-easier-css
date: 2023-12-19
summary: CSS has made some leaps this past year with new features that you can use in your code. This post will share a few of those features you can use to write your CSS in your next project 
tags: ['coding', 'frontend', 'css']
---

![background](./images/blog_bg_12-19.jpg)


I was doing some reading on the interwebs the other day and came across a very interesting article on how CSS is easier to write in 2023, which I have to agree with after reading the article. First things first, I will give credit to the original article [here](https://www.smashingmagazine.com/2023/11/few-ways-css-easier-write-2023/) on Smashing Magazine. It's a great read and gives more CSS tips and tricks you can use while writing your CSS. There were a lot of new features added to CSS this year. It's worth it to do some more digging to find out about the other features that you can now use!

## Centering

Without any further delay. Let's talk about a few ways you can write CSS easier! The first thing we will talk about is centering. There comes a point in your project were. You will have to center a div, text, etc. In the past there was some form of `margin: auto` used to push elements to the middle of the screen. To give an example of what that may look like: 

```CSS
margin-left: auto;
margin-right: auto;
```

This code still works just fine. But, there is an easier way to write this. You can accomplish the same thing using short hand like this: 

```CSS
margin-inline: auto; 
```

I just saved you two lines of code. Feel free to [buy me a coffee](https://www.buymeacoffee.com/aaronjackson). Dairy-free creamer please :-) 


## Trimming Space On The Last Item

Let's say you are building out that navigation section of a website. You often need for the last item not to have any space so that it bumps against the edge of the container div. Of course this only applies if the design of the navigation is aligned left or right of the site. If the navigation is designed to be centered in the site. See the above tip. Here is an example of what the HTML might look like for the navigation: 

```HTML
<nav>
    <ul>
        <li>
            <a href="/about">About</a>
        </li>
        <li>
            <a href="/services">Services</a>
        </li>
        <li>
            <a href="/blog">Blog</a>
        </li>
        <li>
            <a href="/contact">Contact</a>   
        </li>
    </ul>
</nav>

```
Most of the time the navtigation links will be displayed side by side. Assuming you want to add margin for spacing purposes. Simple task right? So you jump into the CSS and do something similar to this: 

```CSS
li {
    display: inline-block;
    margin-inline-end: .5rem;
}
```

This works great for most situations. But, what if later you or the client wants to add another item to the nav? Now you have to either change your code a bit to accommodate the space. What if I told you you can have the browser take care of that? Try this: 

```CSS 
li {
    display: inline-block;
}

li:not(:last-of-type) {
    margin-inline-end: .5rem;
}
```

It's pretty easy to use and it future proofs your code for potentinal changes in the future. 

## Maintaining Proportions 

Proportions! There comes a time when you want that perfect square. In the past we've relied on setting the width and height. Like this: 

```CSS 

height: 600px;
width: 600px;
display: block;
```
This is **OK** but when it comes to responsive design. This can cause issues and make you have to write extra code for different screen sizes. A much more elegant solution would be to use the `aspect-ratio` css property. Like this: 

```CSS 
aspect-ratio: 1;
width: 100%;
```

Now, you have a perfect square no matter the screen size! This cuts down on a lot of code and is much cleaner!

These are just a few ways to write CSS easier. Hopefully, you learned a few things in this post. If not maybe use this as a reference. Can't have too many of those ;-) Have a great day and thanks for reading. Until next time cheers!


