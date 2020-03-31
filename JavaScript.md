----
> Name  : Syed Modassir Ali
> Date  : 30.03.2020
> Title : Javascript
----

# Introduction
JavaScript is a high-level programming language that all modern web browsers support. It is also one of the core technologies of the web

# SYNTAX

Comments helps us make the code easily readable and understoodable by developers.

`// This is a single line comment`

```
/*
* Multi Line comment
*/
```

JavaScript provides 7 different data types undefined, null, boolean, string, symbol, number, and object.
Variables are container address names used to store values.
In JavaScript, we can store a value in a variable using the assignment operator. 
```
var ourVariable = 10;
```

Undefined variables cant be used for operations. Variable names are case sensitive. We generally use camelcase as variable names.

JavaScript variables undergoes mathematical operations like regular variables.

We can use escape sequences or double quoted texts inside single quotes.

`.length` is used to calculate the length of a String. Strings are treated as character array in JavaScript.

In JavaScript, String values are immutable, which means that they cannot be altered once created. 

# Arrays

`var myArray = ["Item1",Number1,.....]`

We can create array of arrays to create multidimensional arrays.
Unlike Strings Arrays are mutable

Data can be added to the end of the array using the push function.

```
var myArray = [1,2,3];
myArray.push(4);
// myArray = [1,2,3,4];
```

pop function is used to remove an element from the end of the array.

```
var myArray = [1,2,3];
var popped = myArray.pop();
// myArray = [1,2];
```
shift function removes element from the first.
unshift works like push function.


----

# Functions

In JavaScript, we can divide up our code into reusable parts called functions.

**SYNTAX**
```
function functionName(param1,param2) {
  console.log("Hello World");
}
```
There are two parts creating the function and calling the function.

Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.

Scope of variable is also important.
