---
layout: post
title: Ultimate NodeJS tutorial for beginners!
image: assets/img/z3.jpg
author: anicode
categories: [ Tutorials, web developement , Nodejs ]
---

# Intoduction

In this tutorial we will be making a simple but efficient Nodejs app named as 'TODO-list-app' that will use Mongo DB for storing data in json like format(No-sql).

# Let's discuss the basics:

 + **Node.js**:

  - It's often used as a “scripting language” for web applications.
  - It is because PYTHON has consistent and simple syntax and the vast library.
  - If you don't have any background in programming, there is no point in using a statically typed language.

  ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# Basic question:

What are different types of errors in Python?

How do you throw an error in Python?

What is difference between error and exception in Python?

How do you ignore an error in Python?

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

So,
## What is nodeJS ?

> Node. js is a platform built on Chrome's JavaScript runtime for easily building fast and scalable network applications.

Node JS is not a programming language, it uses JavaScript language as the main programming interface.

Node runtime can be compared to the JVM Java Virtual Machine or the IDLE Python interpreter.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

### What is best about Nodejs ?

Node. js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

# Wait there are more to clear.

What is node js used for?

Is node js a programming language?

Is node JS frontend or backend?

What is special about node js?


One of the biggest reasons why Node. js is so popular is because it uses JavaScript as its main language to build web applications.

npm install downloads a package and it's dependencies. npm install can be run with or without arguments.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# MongoDB: 

> MongoDB is an open-source document database and leading NoSQL database. MongoDB is written in C++.


What is MongoDB good for?

Is MongoDB better than SQL?

Why is MongoDB called Mongodb?

What big companies use MongoDB?

> MongoDB is great for transactional stores where performance is a concern.

Why is MongoDB called Mongodb?

What big companies use MongoDB?

Why is MongoDB bad?

Why is MongoDB so popular?



> MongoDB is best suitable for hierarchical data storage, but RDBMS is not. 

MongoDB supports JSON query language along with SQL but RDBMS supports SQL query language.

MongoDB uses the MongoDB Query Language (MQL), designed for easy use by developers.

> MongoDB deployments typically use inexpensive, commodity Linux servers that cost as little as $3,000.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# CRUD 

What is CRUD operation API?

What is CRUD operation C#?

What is Java CRUD operation?

Is crud RESTful?

Is rest only for crud?

The ultmate answer to this is:

> 
CRUD stands for "Create, Read, Update, and Delete," which are the four basic database operations.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# What you will be needing?

Have your choice of editor.

+ Installed node.js on your machine.
+ Now lets create a directory as below:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/r56wkybte3v4zuk5lgoq.JPG)

+ Open the folder in your favorite editor

+ Now execute following:

```js
npm init
```

# Packages 

```js
npm install --save express
 mongoose 
 ejs
 dotenv
 ```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

 Proceed them one by one or try this

 ```js

 npm install --save express mongoose ejs dotenv

 ```

# Why there is a need of nodemon ?

nodemon is a tool that helps develop node.js based applications by automatically restarting the node application when file changes.


What is Nodemon in Nodejs?

How do I run node js in node JS?

How do I run Nodemon?

What is the use of Nodemon?

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# Lets code

If you want you may have changes according to your need:

Create a directory and name it as ```package.json```

Source code is below:

```js 
{
  "name": "todo--app",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "nodemon index.js"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "dotenv": "^8.0.0",
    "ejs": "^2.6.1",
    "express": "^4.17.0",
    "mongoose": "^5.5.10"
  },
  "devDependencies": {
    "nodemon": "^1.19.0"
  }
}

```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

> Just copy & paste it.

## Creating index.js file

Open up your app folder and create a ```index.js``` file & copy paste the below code:

```js
const express = require("express");
const app = express();

app.listen(3000, () => console.log("Server Up and running"));

```

> Tip: you can change the port.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# Testing the server

Just type `npm start` and open up your browser and head towards [http:localhost:3000](http:localhost:3000)

See below:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/oar37bcqlz756ytjb0ql.JPG)

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)

# Setting server msgs & methods

Get method will be used as its considered to be the best method
Once this information is submitted, you can see it in your browser’s URL.


now just save this piece of code in your index.js file.

```js
app.get('/',(req, res) => {
res.send('Hello World!');
});
```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/n9jrmekd1qct6mchd9mw.JPG)
