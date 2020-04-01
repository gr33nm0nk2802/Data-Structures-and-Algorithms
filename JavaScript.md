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
Variables which are used without the var keyword are automatically created in the global scope. 
Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

Boolean data types true / false.

# **Conditonal Statements**

if(Condition1)
{
}
else if(condition2)
{
}
else
{
}

In conditionals there is a difference between equality and strict equality.
=== and ==
!== and !=

Logical AND && OR ||


# **SWITCH CASE**

There can be multiple datatypes for case

```
switch (val) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  default:
    defaultStatement;
    break;
}

```

# **Objects**

Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.
Objects are useful for storing data in a structured way, and can represent real world objects, like a cat.

There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.
Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

**Syntax**
```
var myObj = {
  "key1": value1,
  "key2": value 2,
  ...
  "keyN": value N
};
```

Accessing 
```
object.property;
object["property"];
```

Updating
```
object.property = new value;
```

Adding
```
object.newroperty = value;
```

Deleting
```
deleete object.property;
```

Lookup
We can use lookup table of objects to return a specific value for an object.
```
lookup[keyN];
```

Sometimes it is useful to check if the property of a given object exists or not. We can use the `.hasOwnProperty(propname)` method of objects to determine if that object has the given property name. `.hasOwnProperty()` returns `true` or `false` if the property is found or not.
