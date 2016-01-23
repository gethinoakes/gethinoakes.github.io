---
layout: post
title:  "Eloquent JS Notes: Chapter 2 - Program Structure"
date:   2015-11-11
img: russiandolls.jpg
category: development, studying
tags: eloquent javascript, javascript, es6, es5, book, development, studying, developer, software, book notes
---

<note>* This post contains notes that I have written up whilst reading EloquentJS, a free and well-recommended JavaScript book. So it is mainly for my benefit, but if you can take something from it then please do *</note>
<h2>Functions</h2>
Executing a function is called invoking, calling or applying it. Values given to a function are called arguments.
<h2>Return Values</h2>
Functions can also return values, this is called 'to return a value'. Anything that produces a value is an expression, therefore functions that return a value can be used within larger expressions. E.g. <code>console.log(math.min(2,4)+100);&nbsp; // 102</code><!--more-->


<h2>Control Flow</h2>
Statements are executed top to bottom ------&gt;
<h2>Conditional Execution</h2>
We can also choose two different routes based on a boolean value, this is done using an if statement / keyword.

isNaN - returns true if the argument given is NaN.
if/else statements can offer multiple routes.
<h2>While and Do Loops</h2>
A way to repeat code, this form of control flow is called a loop.
<pre class="EnlighterJSRAW" data-enlighter-language="js">var number = 0;
while (number &lt;= 12) {
  console.log(number);  // will count up from 0 in 2's, 0, 2, 4 etc until 12
  number = number + 2;  // could also be written as number += 2;
}</pre>
The while loop executes as long as the expression produces a value that is true when converted to boolean type.

A single loop or if statement can be written without braces.

A 'do' loop differs from a while loop as its body always executes at least once. It starts testing whether it should stop only after its first execution.
<pre class="EnlighterJSRAW" data-enlighter-language="js">do {
  var yourName = prompt('who are you?');
} while (!yourName);</pre>
This will run over and over until a value is entered.
<h2>For Loops</h2>
<pre class="EnlighterJSRAW" data-enlighter-language="js">for (var num=0; num &lt;= 12; num = num + 2) { }</pre>
This is exactly equivalent to the above while loop example, except all the statements are grouped together.

1st part: initialises the loop, usually by defining a variable.
2nd part: expression that checks whether the loop must continue.
3rd part: updates the state of the loop after every iteration.
<h2>Breaking Out of a Loop</h2>
It is possible to use&nbsp;<code>break;</code>&nbsp;in a loop to force it to end if it hits a certain expression. <code>continue;</code> does the opposite by continuing the loop.
<h2>Updating Variables Succintly</h2>
Shortcuts for updating a variables value
<pre class="EnlighterJSRAW" data-enlighter-language="js">+= 1  // adds 1 to the var's value
*=    // multiplies to the var's value
-=    // takes away to the var's value
/=    // divides to the var's value</pre>
<h2>Switch Statements</h2>
Can be used in place of if/else statements, but if/else often looks better (matter of opinion).
<pre class="EnlighterJSRAW" data-enlighter-language="js">switch (expression) {
  case a:
     code to execute
     break;
  case b:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;code&nbsp;to&nbsp;execute
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
  default:
     default code to execute if no case matches
}</pre>
<h2>Summary</h2>
<ul>
	<li>A program is built out of statements (which can contain statements themselves).</li>
	<li>Statements tend to contain expressions (can also contain expressions within expressions)</li>
	<li>Control flow is executed from top to bottom, although this can be disturbed using conditional (if/else and switch) statements or looping (while, do, for) statements.</li>
	<li>Functions encapsulate a piece of program and can be invoked by <code>functionName(argument1, argument2)</code>.</li>
</ul>