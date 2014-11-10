shaping-up-with-angular-js
==========================

Angular JS Fundamentals

## Level 1: Getting started

Why Angular JS?
If you're using Javascript to create a dynamic website, angular is a good choice:

- Angular helps you organize your Javascript
- Angular helps create responsive (as in fact) websites
- Angular plays well jQuery
- Angular is easy to test

What is Angular JS?
A client-side Javascript Framework for adding interactivity to HTML.


Download AngularJS 
http://angularjs.org/ 
We’ll need angular.min.js

Getting started
````html
<!DOCTYPE html>  <html> 
Twitter Bootstrap
￼￼￼<head> 
<link rel="stylesheet" type="text/css" href="bootstrap.min.css" /> 
</head>  <body> 
<script type="text/javascript" src="angular.min.js"></script> 
</body>  </html>
```

#### Modules

- Where we write pieces of our Angular application
- Makes our code more maintainable, testable and readable
- Where we define dependencies for our app

Creating Our First Module

```javascript
var app = angular.module('store', [ ]);
```
store: applicaiton name
[ ] : dependencies (in that case we don't have dependencies)

```html
<!DOCTYPE html>  <html ng-app="store"> 
<head> 
<link rel="stylesheet" type="text/css" href="bootstrap.min.css" /> 
</head>  <body> 
<script type="text/javascript" src="angular.min.js"></script> 
￼Run this module
when the document
```
We use ng-app to bind our application name




#### Expresions
Numerical Operations
```html
<p>
I am {{4 + 6}} 
</p>
```
String Operations
```html
<p>
{{"hello" + " you"}} 
</p>
```
+ More Operations: http://docs.angularjs.org/guide/expression


#### Controllers

Controllers are where we define our app's behavior by defining functions and values.

```javascript
(function(){
 var app = angular.module('store', [ ]);
 app.controller('StoreController', function(){

 });

});
```

We can also store data inside a controller

```javascript
(function(){
 var app = angular.module('store', [ ]);
 app.controller('StoreController', function(){
   this.product = gem;
 });
 
 var gem = { 
   name: 'Dodecahedron',  price: 2.95,  description: '. . .', 
  }

});
```

Attaching our controller in a html page

```html
<body> 
<div ng-controller="StoreController as store"> 
￼<h1> {{store.product.name}} </h1>
<h2> {{store.product.price}} </h2>
<p> {{store.product.description}} </p>
</div>
</body>
```


## Level 3: Forms, Models and Validations

### Introducing ng-model

ng-model binds the form element value to the property

Examples:

With a Checkbox
```html
<input ng-model="review.terms" type="checkbox" /> I agree to the terms
```
Sets value to true or false


