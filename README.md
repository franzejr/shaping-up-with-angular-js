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
- 

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


## Level 3: Forms, Models and Validations

### Introducing ng-model

ng-model binds the form element value to the property

Examples:

With a Checkbox
```html
<input ng-model="review.terms" type="checkbox" /> I agree to the terms
```
Sets value to true or false


