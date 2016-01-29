---
layout: post
title: "Eloquent JS Notes: Chapter 3 - Functions"
date: 2015-11-13
img: js.jpg
category: development, studying
tags: eloquent javascript, javascript, es6, es5, book, development, studying, developer, software, book notes
---

<note>* This post contains notes that I have written up whilst reading EloquentJS, a free and well-recommended JavaScript book. So it is mainly for my benefit, but if you can take something from it then please do *</note>
<h2>Defining a Function</h2>
<pre class="EnlighterJSRAW" data-enlighter-language="js">var square = function(x) {
  return x * x;
} 
square(12) // 144</pre>
Functions have a set of parameters and a body, can have multiple parameters or none. Where a value is returned the return keyword must be used.
<h2>Parameters and Scopes</h2>
Parameters of a function behave like regular variables but their initial values are set by calling the function, not in the function itself.<!--more-->Variables and parameters created inside functions are local to them and cannot be used outside the function, where they are declared using the <code class="EnlighterJSRAW" data-enlighter-language="js">var</code> keyword.

Variables declared outside of any function are global and can be used/accessed within functions.
<pre class="EnlighterJSRAW" data-enlighter-language="js">var x = 'outside'

var f1 = function() {
  var x = 'inside f1'
}
f1();  // inside f1
console.log(x)  // outside

var f2 = function() {
  x = 'inside f2';
}
f2();  // inside f2
console.log(x)  // inside f2</pre>
This helps to avoid/prevent accidental interference between functions and variables.
<h2>Nested Scope</h2>
JS can distinguish between global and local variables, but functions can also be created within other functions.

As of ES5 functions are only capable of creating new scope, this will change with <a href="http://es6-features.org/#BlockScopedFunctions" target="_blank">ES6</a> with the introduction of the 'let' keyword.
<h2>Functions as Values</h2>
A function can do all the things that other variable values can.
<h2>Declaration Notation</h2>
Functions can also be declared without a variable being assigned. Function declarations are not part of the regular top-to-bottom flow of control, they are conceptually moved to the top of their scope and can be used by all code within that scope.

* Don't put function definitions inside conditional statements (if, loop etc.)
<h2>The Call Stack</h2>
Everytime a function is called, the current context is put into the call stack, when it returns it removes itself from the stack.

When the stack grows too big, the computer will fail with a message like "out of space" or "too much recursion".
<h2>Optional Arguments</h2>
If you pass a function more arguments that it takes JS will simply ignore the extra arg's.
If you don't pass enough arg's then JS will assign the missing parameters as undefined.

Downside of this is you could pass the wrong number or arg's and not know.
Upside is this behaviour can be used to take optional arg's.
<h2>Recursion</h2>
Recursion is when a function calls itself, recursive functions can be a lot slower than just using a loop or similar, however they may look more elegant and can consist of less code.

Some programs are easier to write with recursion rather than using loops.
<h2>Growing Functions</h2>
Functions can come from writing similar code over and over, or by deciding on some functionality that will need one and we may have started writing for already.

Try to use names that make sense.
Don't add too much 'cleverness' to a function, resist the urge to write little frameworks everywhere.
<h2>Functions and Side Effects</h2>
Functions can be divided into those hat return side effects or return a value (they can also do both).

Functions that return something are more useful and can be used by more code and are easier to combine.
Pure functions always return the same thing. Non-pure may return different values based on all kinds of factors.
<h2>Summary</h2>
<ul>
	<li>Function keyword when used as an expression can create a function value.</li>
	<li>When used as a statement it can be used to declare a variable and give it a function as its value.</li>
</ul>
<pre class="EnlighterJSRAW" data-enlighter-language="js">// create a function value
var f = function(a) {
  console.log(a+2);
}

// declare 'g' to be a function
function g(a, b) {
  return a * b * 3.5;
}</pre>
<ul>
	<li>Key aspect in understanding functions is understanding local scope.
<ul>
	<li>Parameters and variables declared inside a function are local to that function, re-created each function call and not visiable from outside.</li>
	<li>Functions declared inside another function have access to the other functions scope (variables etc.).</li>
</ul>
</li>
	<li>Functions help to stop repeating code and can make code more readable.</li>
</ul>