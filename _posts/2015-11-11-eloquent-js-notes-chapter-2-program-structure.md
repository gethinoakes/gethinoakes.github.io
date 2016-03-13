---
layout: post
title:  "Eloquent JS Notes: Chapter 2 - Program Structure"
date:   2015-11-11
category: development, studying
desc: "Eloquent JS Notes: Chapter 2 - Program Structure"
keywords: "javascript, eloquent javascript, development, program structure, studying, tutorial"
---

## Functions
Executing a function is called invoking, calling or applying it. Values given to a function are called arguments.


## Return Values
Functions can also return values, this is called 'to return a value'. Anything that produces a value is an expression, therefore functions that return a value can be used within larger expressions. E.g.

~~~js
console.log(math.min(2,4)+100); // 102
~~~


## Control Flow
Statements are executed top to bottom


## Conditional Execution
We can also choose two different routes based on a boolean value, this is done using an if statement / keyword.

isNaN - returns true if the argument given is NaN.
if/else statements can offer multiple routes.


## While and Do Loops
A way to repeat code, this form of control flow is called a loop.

~~~js
var number = 0;
while (number &lt;= 12) {
  console.log(number);  // will count up from 0 in 2's, 0, 2, 4 etc until 12
  number = number + 2;  // could also be written as number += 2;
}
~~~

The while loop executes as long as the expression produces a value that is true when converted to boolean type.

A single loop or if statement can be written without braces.

A 'do' loop differs from a while loop as its body always executes at least once. It starts testing whether it should stop only after its first execution.

~~~js
do {
  var yourName = prompt('who are you?');
} while (!yourName);
~~~

This will run over and over until a value is entered.


## For Loops
~~~js
for (var num=0; num &lt;= 12; num = num + 2) { }
~~~

This is exactly equivalent to the above while loop example, except all the statements are grouped together.

**1st part:** initialises the loop, usually by defining a variable.

**2nd part:** expression that checks whether the loop must continue.

**3rd part:** updates the state of the loop after every iteration.


## Breaking Out of a Loop
It is possible to use `break;` in a loop to force it to end if it hits a certain expression. `continue;` does the opposite by continuing the loop.


## Updating Variables Succintly
Shortcuts for updating a variables value

~~~js
+= 1  // adds 1 to the var's value
*=    // multiplies to the var's value
-=    // takes away to the var's value
~~~


## Switch Statements
Can be used in place of if/else statements, but if/else often looks better (matter of opinion).

~~~js
switch (expression) {
  case a:
     // code to execute
     break;
  case b:
    // code to execute
    break;
  default:
     // default code to execute if no case matches
}
~~~


## Summary
- A program is built out of statements (which can contain statements themselves).
- Statements tend to contain expressions (can also contain expressions within expressions)
- Control flow is executed from top to bottom, although this can be disturbed using conditional (if/else and switch) statements or looping (while, do, for) statements.
- Functions encapsulate a piece of program and can be invoked by `functionName(argument1, argument2)`