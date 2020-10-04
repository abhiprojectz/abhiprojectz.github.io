---
layout: post
title: Remove all console messages in just one line!
image: assets/img/p16.jpg
author: anicode
categories: [ Tutorials, web developement ]
---

Ever wonder how to hide all the console messages in any text renderer in a very short span of time that's too quickly?

Then here is a *PRO TIP!*


## Welcome to abhi codes blog.

![](https://raw.githubusercontent.com/abhiprojectz/CSS-Generator/master/assets/unnamed%20(2).gif)




![](https://raw.githubusercontent.com/abhiprojectz/CSS-Generator/master/assets/unnamed%20(4).gif)

Just use this one line of code!

```
console.log = function() {};

```

It will hide the console to open!

This command converts console function into an empty function resulting in "" empty string! 





# More advanced way

You can create a function to hide the console at your convenience works even in IE<7 

```
var logger = function()
{
    var oldConsoleLog = null;
    var pub = {};

    pub.enableLogger =  function enableLogger() 
                        {
                            if(oldConsoleLog == null)
                                return;

                            window['console']['log'] = oldConsoleLog;
                        };

    pub.disableLogger = function disableLogger()
                        {
                            oldConsoleLog = console.log;
                            window['console']['log'] = function() {};
                        };

    return pub;
}();

```

You can call the function as ```enableLogger()``` or ```disableLogger()``` as per your project convenience!

Hope this small tip helps you!

*Happy coding!*

