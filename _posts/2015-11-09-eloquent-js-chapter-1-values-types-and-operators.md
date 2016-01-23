---
layout: post
title:  "Eloquent JS Notes: Chapter 1 - Values, Types, and Operators"
date:   2015-11-09 19:00:00 +0000
img: js.jpg
category: development, studying
tags: eloquent javascript, javascript, es6, es5, book, development, studying, developer, software, book notes
---

<note>* This post contains notes that I have written up whilst reading EloquentJS, a free and well-recommended JavaScript book. So it is mainly for my benefit, but if you can take something from it then please do *</note>


## Unary Operators
Some operators are words instead of symbols (+, - etc.). Such as typeof which returns the type of the value you give it. For example...
{% highlight javascript %}
console.log(typeof 4);   // number
console.log(typeof '4'); // string
{% endhighlight %}


## Boolean Comparisons
Comparison is based on unicode standard, uppercase letters are always 'less' than lowercase. I.e. 'Z' &lt; 'z' = true.


## Logical Operators
{% highlight javascript %}
||  // OR
&&  // AND
!   // NOT
{% endhighlight %}

There is another logical operator named Ternary. It can be used to create quick and short if statements by using a question mark and a semicolon. It is a conditional operator, the value on the left of the ? picks which of the two values will come out. When the conditional expression is true the left value will come out, when false the right value.

{% highlight javascript %}
var num = 1;
var total = num + num;
console.log(num=2 ? 2 : 3);  // returns 2 as the expression (1+1=2) is true
{% endhighlight %}


## Undefined Values
null & undefined denote the absence of a meaningful value. They are both values themselves but will never contain any information.


## Automatic Type Conversion
JS will go out of its way to accept almost any program instead of spitting out errors, always converting the value to the type it wants if an operator is applied to the wrong type of value. This is called type coercion.
{% highlight javascript %}
console.log(8 * null)    // 0
console.log('5' - 1)     // 4
console.log('5' + 1)     // '51'
console.log('five' * 2)  // NaN (not a number)
console.log(false == 0)  // true
{% endhighlight %}

Use absolute comparison to protect against type coercion if needed (===).


## Short-Circuiting of Logical Operators
|| Will return the value on the left if it is true, right if it is false.
&& Will return value to the left if it is false, right if it is true. 
This allows || to be used as a way to fall back on a default value, && works similarly but opposite. For example:
{% highlight javascript %}
console.log(true || 'gethin');    // true
console.log(false || 'gethin');   // gethin
console.log(true && 'gethin');    // gethin
console.log(false && 'gethin');   // false
{% endhighlight %}


## Summary
<ul>
	<li>Values are created by typing in their name (true, null) or value (13, 'abc')</li>
	<li>Values can be combined and transformed with operators</li>
</ul>