---
layout: post
title:  "EJS Chapter 4: Datastructures - Objects & Arrays"
date:   2015-12-21
img: js.jpg
category: development, studying
tags: eloquent javascript, javascript, es6, es5, book, development, studying, developer, software, book notes
---

## Data Sets
Arrays are used to hold data sets in square brackets.

```js
var listOfNumbers = [2, 3, 5, 7, 11];
listOfnumbers[0]; // 2
```

## Properties
myString.length, Math.max etc. are expressions that access a property of some value. <code>.length</code> accesses the length property of the string for example.
null and undefined don't have any properties and will return as error if you try, almost all other JS values do.

Most common ways to access are dot notation and square brackets. <code>value.x</code> and <code>value[x]</code> access a property's value but not necessarily the same property. The difference is how 'x' is interpreted:
<ul>
	<li>When using dot notation, the 'x' must be a valid variable name which directly names the property.
<ul>
	<li><code>value.x</code> fetches the property of value named 'x'</li>
</ul>
</li>
	<li>When using brackets, the expression 'x', is evaluated to get the property name.
<ul>
	<li><code>value[x]</code> tries to evaluate the expression 'x' and sues the result as the property name.</li>
</ul>
</li>
</ul>
## Methods
Properties that contain functions are called methods of the value they belong to, such as "uppercase is a method of a string".
Array objects have methods such as:
<pre class="EnlighterJSRAW" data-enlighter-language="js">.push  // adds values to the end of arrays
.join  // joins array values into one
.pop  // removes a value from the end of an array
</pre>
Properties inside objects are separated by commas, properties whose names are not valid variable names or numbers have to be quoted.
Can assign properties to an object with the = operator, it will replace an already existing value or create a new property.

## Mutability
Values discussed by this chapter such as number, strings and booleans are all 'immutable' meaning it is impossible to change the existing value of these types.
You can combine them and create new values, but the specific string would always be the same value.

It is not possible to select a character in a string to change the whole word / string value.

However the content of object values can be modified by changing their properties.
<pre class="EnlighterJSRAW" data-enlighter-language="js">var object1 = { value: 10};
var object2 = object1;
var object3 = { value: 10};

console.log(object1 == object2);  // true
console.log(object1 == object3);  // false

object1.value = 15;
console.log(object2.value);  // 15;
console.log(object3.value);  // 10;
</pre>
JS's == operator only returns true when comparing objects if both objects are precisely the same value, comparing different objects will return false even if they have identical contents.

### Example of Object in a function
<pre class="EnlighterJSRAW" data-enlighter-language="js">var journal = [];

function addEntry (events, didITurn) {
  function.push ({
    events:events,
    squirrel: didITurn
  });
}

addEntry(['work', 'true', 'pizza'], false);
</pre>
## Objects as Maps
A map is a way to go from values in one domain to corresponding values in another domain, e.g:
<pre class="EnlighterJSRAW" data-enlighter-language="js">var map = {};
function store(event, value) {
  map[event] = value;
}

for (var event in map) {
  console.log(event + ' ' + map[event]);
}

</pre>
## Further Arrayology
<pre class="EnlighterJSRAW" data-enlighter-language="js">var toDoList = [];
toDoList.shift;  // remove from start of array
toDoList.unshift;  // add at start of array

console.log([1, 2, 3, 4, 1]).indexOf(2));  // 1
console.log([1, 2, 3, 4, 1]).lastIndexOf(2));  // 3
</pre>
Both can take a 2nd argument (optional) to indicate when to start searching from.

<code>.slide()</code> takes a start and end index and returns an array of values in between.
<pre class="EnlighterJSRAW" data-enlighter-language="js">console.log([0, 1, 2, 3, 4].slice(2, 4)); // [2, 3]
console.log([0, 1, 2, 3, 4].slice(2));  // [2, 3, 4]
</pre>
This also has the similar effect on strings.

<code>.concat()</code> can be used to glue arrays together, example below shows concat with slice.
<pre class="EnlighterJSRAW" data-enlighter-language="js">function remove(array, index) {
  return array.slice(0, index).concat(array.slice(index+1));
}
console.log(remove(['a', 'b', 'c', 'd', 'e'], 2));
// ['a', 'b', 'd', 'e']
</pre>
## Strings and their Properties
Values of type string, number and boolean are not objects and so are immutable, meaning that you can't assign them properties, however they do have some built in.
<pre class="EnlighterJSRAW" data-enlighter-language="js">console.log('coconuts'.slice(4, 7));  // nut
console.log('coconuts'.indexOf('a'));  // 5
</pre>
.indexOf() on a string can take a string containing more than one character, whereas on an array it can only look for a single element.
<pre class="EnlighterJSRAW" data-enlighter-language="js">console.log('one two three').indexOf('ee'));  // 11
</pre>
<code>.trim()</code> removes whitespace (spaces, newlines, tabs and similar characters) from start and end.
<pre class="EnlighterJSRAW" data-enlighter-language="js">console.log('      trim\n   ').trim());  // trim
</pre>
<code>.charAt()</code> returns the character at the specified index.
<pre class="EnlighterJSRAW" data-enlighter-language="js">console.log('hello').charat(2));  // l
</pre>
Can also be done with bracket notation ([]).
<pre class="EnlighterJSRAW" data-enlighter-language="js">var string = 'hello';
console.log(string[2]);  // e
</pre>
## The Arguments Object
When a function is called a special var 'arguments' is added to the environment in which the function body runs. It refers to an object that holds all the arguments passed to the function.
<pre class="EnlighterJSRAW" data-enlighter-language="js">function argumentCounter() {
  console.log('there are ' + arguments.length + 'args in this function call');
}

argumentCounter(1, 'hello', 4);  // there are 3 args in this function call
</pre>
This can be used to improve functions and make them easier to call where an array is used for example.
<h2>Summary</h2>
<ul>
	<li>Objects and arrays provide ways to group several values into one.</li>
	<li>Most values in JS have properties (except null and undefined) and are accessed via either dot or square bracket notation e.g. <code>value.groupName</code> or <code>value[groupName]</code></li>
	<li>Methods are functions that live in properties and (usually) act as the value they are a property of.</li>
	<li>Objects as maps associate values with names and the 'in' operator can be used to find out whether an object contains a property with a given name.</li>
</ul>