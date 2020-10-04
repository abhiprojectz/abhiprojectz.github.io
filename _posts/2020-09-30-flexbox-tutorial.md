---
layout: post
title: The ultimate guide to master flexbox in 10minutes
image: /assets/img/p3.jpg
author: anicode
categories: [ Projects, web development ] 
featured: true
hidden: true
---
The CSS flexbox (Flexible Box Layout Module) is a layout module consisting of the flex container (the parent element) and the flex elements (the elements for children).



![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/hwhhv135qzg03440ugrw.jpg)



 The flex objects can be arranged as a row or as a column, and the free space available between them can be distributed in different ways.
 
 Share this with your freinds using on twitter 
 #CSSCheatz
 
 
 ## Basic Example:
 
 

 ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zln0j9q5qpczqslqu5km.jpg)
 
 
 
 ```
 .container {
  display: flex;
}
.container > elem {
  flex: 1 1 auto;
}

```
 
 
 The Flexbox layout is optimised for small-scale layouts, whereas the Grid layout is better adapted for larger-scale layouts.



## Display 

```
display: flex;
display: inline-flex;
 
  ```


 By example, all flex objects may try to fit in one section. You can adjust that, and with this property allow the products to wrap as required.
 
 ## Flex- Direction 
 
 
 ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/olgmhc0rvzhsww24v9la.png)
 
 
 ```
 
 flex-direction: row;            
  flex-direction: row-reverse;    
  flex-direction: column;         
  flex-direction: column-reverse; 
  
  ```
  
  ## Wrap
  
  **One line**

```
 flex-wrap: nowrap; 
 ```
 
 **Multiline**
 
 ```
  flex-wrap: wrap;   
  
  ```
  
  ## Alignment
  
  
  ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/6ch0rdd0nuaahlkqskbx.png)
  
  
  
  **vertical-align to top**
  
  
  ```
  align-items: flex-start; 
```

**vertical-align to bottom **

```
  align-items: flex-end;  

```
**vertical-align to center**


```
  align-items: center;   
  
  ```
  
  **To eg height**
  
  ```
  align-items: stretch; 

```   

## Refer this graphic

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/9l6d40epptjm6p4y3e7z.png)



# Justify content

```
  justify-content: flex-start;    
  ```
 

 ```
 
  justify-content: center;   

```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/6wsan1ti10rwwg51af1w.jpg)


      
```
 
  justify-content: flex-end;  

```
     
     
```
 
  justify-content: space-between; 

```
 
 
 ```
 
  justify-content: space-around;

```
   
   
```
 
  justify-content: space-evenly;  
  
```
 
 
 # Flex child
 
 
 ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/rlllec8rafcwj8ldu6rx.png)
 
 
 ## simple
 
 
 ```
 
  flex: 1 0 auto;
```
 
  
  **Flex grow,shrink.,**
  
  ```
 
  
  
  flex-grow: 1;
  flex-shrink: 0;
  flex-basis: auto;
  
  ```
 
 
 **Order**
 
 ```
 
  order: 1;
  order:2;
  ```
 
  
  ## Align self
  
  **left**
  
  ```
 
  align-self: flex-start;  
  
  ```
 
  **right**
  
  ```
 
  margin-left: auto;       
  ```
 
  
  
  # Small devices layouts
  
  
  ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ofpefs8dg9gmht502fau.png)
  
  
  **Simple way that fits small sized devices best!**
  
  
  ```
 
  
  .container {
  display: flex;
  flex-direction: column;
}

.container > .header {
  flex: 0 0 100px;
}

.container > .MainContent {
  flex: 1 0 auto;
}
  ```
 
 # Arrange elements in a table
 
 
```
 .container {
  display: flex;
}


.container > .box1 { flex: 1 0 20%; }
.container > .box2 { flex: 1 0 40%; }
.container > .box3    { flex: 1 0 250%; }
```




# Centering vertically using flex


![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/wew2moloxqed9z6fkzma.png)


```
  
.container {
  display: flex;
}

.container > div {
  width: 100px;
  height: 100px;
  margin: auto;
}

```
 
  For more cheatsheets like this follow me on [twitter](https://twitter.com/abhiprojectz)
  
  
  

