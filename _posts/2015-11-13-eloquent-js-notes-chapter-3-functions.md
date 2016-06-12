---
layout: post
title: "Eloquent JS Notes: Chapter 3 - Functions"
date: 2015-11-13
tags: [development]
desc: "Eloquent JS Notes: Chapter 3 - Functions"
keywords: "javascript, eloquent javascript, functions, development, studying, tutorial"
---

## Defining a Function
~~~js
var square = function(x) {
  return x * x;
}
square(12) // 144
~~~

Functions have a set of parameters and a body, can have multiple parameters or none. Where a value is returned the return keyword must be used.


## Parameters and Scopes
Parameters of a function behave like regular variables but their initial values are set by calling the function, not in the function itself. Variables and parameters created inside functions are local to them and cannot be used outside the function, where they are declared using the `var` keyword.

Variables declared outside of any function are global and can be used/accessed within functions.

~~~js
var x = 'outside'

var f1 = function() {
  var x = 'inside f1'
}
f1();  // inside f1
console.log(x)  // outside

var f2 = function() {
  x = 'inside f2';
}
f2();  // inside f2
console.log(x)  // inside f2
~~~

This helps to avoid/prevent accidental interference between functions and variables.


## Nested Scope
JS can distinguish between global and local variables, but functions can also be created within other functions.

As of ES5 functions are only capable of creating new scope, this will change with [ES6](http://es6-features.org/#BlockScopedFunctions) with the introduction of the `let` keyword.


## Functions as Values
A function can do all the things that other variable values can.


## Declaration Notation
Functions can also be declared without a variable being assigned. Function declarations are not part of the regular top-to-bottom flow of control, they are conceptually moved to the top of their scope and can be used by all code within that scope.

- Don't put function definitions inside conditional statements (if, loop etc.)


## The Call Stack
Everytime a function is called, the current context is put into the call stack, when it returns it removes itself from the stack.

When the stack grows too big, the computer will fail with a message like "out of space" or "too much recursion".


## Optional Arguments
If you pass a function more arguments that it takes JS will simply ignore the extra arg's.
If you don't pass enough arg's then JS will assign the missing parameters as undefined.

Downside of this is you could pass the wrong number or arg's and not know.
Upside is this behaviour can be used to take optional arg's.


## Recursion
Recursion is when a function calls itself, recursive functions can be a lot slower than just using a loop or similar, however they may look more elegant and can consist of less code.

Some programs are easier to write with recursion rather than using loops.


## Growing Functions
Functions can come from writing similar code over and over, or by deciding on some functionality that will need one and we may have started writing for already.

Try to use names that make sense.
Don't add too much 'cleverness' to a function, resist the urge to write little frameworks everywhere.


## Functions and Side Effects
Functions can be divided into those hat return side effects or return a value (they can also do both).

Functions that return something are more useful and can be used by more code and are easier to combine.
Pure functions always return the same thing. Non-pure may return different values based on all kinds of factors.

## Summary
- Function keyword when used as an expression can create a function value.
- When used as a statement it can be used to declare a variable and give it a function as its value.

~~~js
// create a function value
var f = function(a) {
  console.log(a+2);
}

// declare 'g' to be a function
function g(a, b) {
  return a * b * 3.5;
}
~~~

- Key aspect in understanding functions is understanding local scope:
	- Parameters and variables declared inside a function are local to that function, re-created each function call and not visiable from outside.
	- Functions declared inside another function have access to the other functions scope (variables etc.).
- Functions help to stop repeating code and can make code more readable.
