---
layout: post
title: Ultimate 2 line trick to make your document fully responsive!
image: /assets/img/p11.png
author: anicode
categories: [ Tutorials, web developement ]
---

Every individual who's a web engineer ought to see how to make their site receptive to even the littlest degree. It's normal that all that is right now carefully accessible will be versatile benevolent in some conceivable manner or it seems like your site and aptitudes are fairly out dated. 


So I made a brisk beginning aide on the most proficient method to make your site negligibly responsive by adding just two things to your CSS document.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/fxgk30aprhpq7qn6439g.jpg)

# In Brief

The manner in which you begin to make your site jekylli, is by utilizing rates for your tallness and width rather than static pixel sizes. This way when somebody resizes their program window, your html labels will shrivel or grow appropriately as opposed to breaking the page. 


## What's happening?

The principal thing to acknowledge about Responsive plan. This means your site parts should scale with your screen size.


## Don't do this

```
div {
  width: 25px;
  height: 50px;
}

```

Never try to size your elements in pixel ratio.

{: .box-note}
If you are struggling dealing with **shadows**, **borders** etc html parametric elements then you may have a look on our css generator tool!

[css-generator](http://anicode.in/CSS-Generator)


## Do this:


```

div {
  width: 25%;
  height: 50%;
}

```


The following will scale based on the percentage of your screen.

# Next

Don't forget to create a **media-scale** screen meta tag inside the ```<head></head>``` of your document file.

This will cause your CSS file to be use in  different CSS styles based on the screen size of the device its on.

Embed this code in your ```.html``` file

```

<meta name="viewport" content="width=device-width, initial-scale=1.0">

```


Remember this will not make your project look responsive on various platform.

# Usage of the media query inside css file




```

@media screen and (max-width: 450px) { 
  /* CSS Code for when the screen size is 480px Screen size */
}

```

At 450px width and below, that line will cause every screen to apply the CSS code to your website between the curly brackets. This way, the css styles will refer to themselves if the website is on a mobile screen, which is typically less than 450px wide.


## keypoint

This is just amazing you can test this on pc by resizing your chrome's (browser's) windows an see it in action.


```

div {
  width: 300px;
  height: 300px;
  color: yellow;
}

@media screen and (max-width: 780px) {
 
  div {
    color: green;
  }
}

```

Here are some important media queries used widely.
keep it in your pocket.

### For Desktop:



```
@media screen and (max-width: 1000px) { /* Desktop */ }

```

### For Tablet:

```
@media screen and (max-width: 780px) { /* tablet */ }

```

### For mobile:


```
@media screen and (max-width: 480px) { /* mobile */ }

```

# At last

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/wu5hiruds40w1dex1s58.gif)


Remember to subscribe to our newsletter to get the latest updates right to your mailbox!

## Optional

if you want little updates then do follow me on twitter.

Hope's this article helps you.
