---
layout: post
title: How to create a very basic REST Api in Nodejs 2021 
image: assets/img/p16.jpg
author: anicode
categories: [ Tutorials, web developement ]
---



Nodejs Rest API Example Using ExpressJS and Mysql.

I have created simple example to create RESTFul api for crud operation using mysql database.

I have added following features into this source code:

+ Add Record using rest call into mysql database
+ Edit Record using rest call into mysql database
+ Delete Record using rest call into mysql database
+ Featch records using rest call into mysql database
+ how to create table in db
+ You need to craete 'test' database into mysql and import customer.sql table into your mysql database.

# How to run nodejs application:

Firstly copy `index.js` and `package.json` file into your nodejs project folder.

> Open command line and cd to your above nodejs project folder

```js
run npm install

run node index.js
```

Lets build the main part of our project.

These are main variables to be defined.

```js
var http = require("http");
var express = require('express');
var app = express();
var mysql      = require('mysql');
var bodyParser = require('body-parser');
```

The mysql part starts here be sure to download and fully install the mysql in your system.


```js
//start mysql connection
var connection = mysql.createConnection({
  host     : 'localhost', //mysql database host name
  user     : 'root', //mysql database user name
  password : '', //mysql database password
  database : 'test' //mysql database name
});

connection.connect(function(err) {
  if (err) throw err
  console.log('You are now connected with mysql database...')
})

//end mysql connection

//start body-parser configuration
app.use( bodyParser.json() );       // to support JSON-encoded bodies
app.use(bodyParser.urlencoded({     // to support URL-encoded bodies
  extended: true
}));
//end body-parser configuration
```


Lets create the app server this is going to be very basic http server.

```js
var server = app.listen(3000,  "127.0.0.1", function () {

  var host = server.address().address
  var port = server.address().port

  console.log("Example app listening at http://%s:%s", host, port)

});
```


The rest api to get all customers.

```js
app.get('/customer', function (req, res) {
   connection.query('select * from customer', function (error, results, fields) {
	  if (error) throw error;
	  res.end(JSON.stringify(results));
	});
});
```

The get request using our api, rest api to get a single customer data.

```js
app.get('/customer/:id', function (req, res) {
   connection.query('select * from customers where Id=?', [req.params.id], function (error, results, fields) {
	  if (error) throw error;
	  res.end(JSON.stringify(results));
	});
});
```

rest api to create a new customer record into mysql database

```js
app.post('/customer', function (req, res) {
   var params  = req.body;
   console.log(params);
   connection.query('INSERT INTO customer SET ?', params, function (error, results, fields) {
	  if (error) throw error;
	  res.end(JSON.stringify(results));
	});
});
```


Rest api to update record into mysql database

```js
app.put('/customer', function (req, res) {
   connection.query('UPDATE `customer` SET `Name`=?,`Address`=?,`Country`=?,`Phone`=? where `Id`=?', [req.body.Name,req.body.Address, req.body.Country, req.body.Phone, req.body.Id], function (error, results, fields) {
	  if (error) throw error;
	  res.end(JSON.stringify(results));
	});
});
```


rest api to delete record from mysql database

```js

app.delete('/customer', function (req, res) {
   console.log(req.body);
   connection.query('DELETE FROM `customer` WHERE `Id`=?', [req.body.Id], function (error, results, fields) {
	  if (error) throw error;
	  res.end('Record has been deleted!');
	});
});
```
This is our end of very basic rest api.

Now lets create one file to create mysql database table , dont worry all the stuff is give below.

```
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;

--
-- Database: `test`
--

-- --------------------------------------------------------

--
-- Table structure for table `customer`
--

CREATE TABLE IF NOT EXISTS `customer` (
  `Id` int(11) NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) NOT NULL,
  `Address` varchar(255) NOT NULL,
  `Country` varchar(100) NOT NULL,
  `Phone` int(10) NOT NULL,
  `Created_on` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `Updated_on` datetime NOT NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`Id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 AUTO_INCREMENT=1 ;
```


Hope , this post helps you be sure to read all my posts.
