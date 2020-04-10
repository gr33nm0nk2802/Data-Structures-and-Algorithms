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

```
JSON.stringify(); // converts array to string
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
delete object.property;
```

Lookup
We can use lookup table of objects to return a specific value for an object.
```
lookup[keyN];
```

Sometimes it is useful to check if the property of a given object exists or not. We can use the `.hasOwnProperty(propname)` method of objects to determine if that object has the given property name. `.hasOwnProperty()` returns `true` or `false` if the property is found or not.


An Object is a flexible data Structure which allows for arbitary combination of data.
We can also create an array of objects. Object of Objects, Object of Arrays and so on...


JSON is a related data interchange format used to store data.
 
Sub properties of any object can be accessed by using sequence of `[]` and `.` dot notion.

### Solution to Records problem

```
// Setup
var collection = {
  2548: {
    album: "Slippery When Wet",
    artist: "Bon Jovi",
    tracks: [
      "Let It Rock",
      "You Give Love a Bad Name"
    ]
  },
  2468: {
    album: "1999",
    artist: "Prince",
    tracks: [
      "1999",
      "Little Red Corvette"
    ]
  },
  1245: {
    artist: "Robert Palmer",
    tracks: [ ]
  },
  5439: {
    album: "ABBA Gold"
  }
};

// Only change code below this line
function updateRecords(id, prop, value) {

  if(value==="") delete collection[id][prop];

  else if(prop==="tracks"){
    // if property is track it updates it to an array or creates an empty array.
    collection[id][prop] = collection[id][prop] || [];
    collection[id][prop].push(value);
  }

  else
  collection[id][prop]=value;
  return collection;
}

console.log(updateRecords(5439, "artist", "ABBA"));

```

# Loops

while loop

```
while(condition){
  // body of the loop 
}
```

for loop

```
for ([initialization]; [condition]; [final-expression])
```

Nested Loops

do-While loops

```
do
{
  //body of the loop
}while(condition);
```

# Recursion

```
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```

`Math.random();`    `Math.floor();`
`Math.floor(Math.random() * (max - min + 1)) + min`

Use parseInt() in the convertToInteger function so it converts the input string str into an integer, and returns it.

parseInt(string, radix);

radix accepts values between 2 to 36.

# Ternary

`condition ? statement-if-true : statement-if-false;`

-----
-----

# ES6

ECMAScript is a standardized version of JavaScript with the goal of unifying the language's specifications and features. As all major browsers and JavaScript-runtimes follow this specification, the term ECMAScript is interchangeable with the term JavaScript.


----

let keyword helps us create a vraibale within the local scope and also helps us avoid multiple variable declaration.

const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned.

Common convention is to name const variables with ALL CAPS.

objects (including arrays and functions) assigned to a variable using const are still mutable.

To ensure your data doesn't change, JavaScript provides a function `Object.freeze` to prevent data mutation.Once the object is frozen, you can no longer add, update, or delete properties from it. Any attempt at changing the object will be rejected without an error.


## Arrow Function

In JavaScript, we often don't need to name our functions, especially when passing a function as an argument to another function. Instead, we create inline functions. We don't need to name these functions because we do not reuse them anywhere else.

```
const myFunc = function() {
  const myVar = "value";
  return myVar;
}

```

ES6 provides us with the syntactic sugar to not have to write anonymous functions this way. Instead, you can use arrow function syntax:

```
const myFunc = () => {
  const myVar = "value";
  return myVar;
}
```

When there is no function body, and only a return value, arrow function syntax allows you to omit the keyword return as well as the brackets surrounding the code. This helps simplify smaller functions into one-line statements:

```
const myFunc = () => "value";
```

**SOLUTION**

```
const magic = () => {
  "use strict";
  return new Date();
};
```

Just like a regular function, you can pass arguments into an arrow function.

```
// doubles input value and returns it
const doubler = (item) => item * 2;

// the same function, without the argument parentheses
const doubler = item => item * 2;

// multiplies the first input value by the second and returns it
const multiplier = (item, multi) => item * multi;
```

In order to help us create more flexible functions, ES6 introduces default parameters for functions. This default parameter kicks in when the argument is not specified.
```
const increment = (number, value=1) => number + value;
```

In order to help us create more flexible functions, ES6 introduces the **rest parameter** for function parameters. With the rest parameter, you can create functions that take a variable number of arguments. These arguments are stored in an array that can be accessed later from inside the function.

The rest parameter syntax allows us to represent an indefinite number of arguments as an array.

```
function sum(...Args) {
  return theArgs.reduce((previous, current) => {
    return previous + current;
  });
}

console.log(sum(1, 2, 3));
// expected output: 6
```

ES6 introduces the **spread operator**, which allows us to expand arrays and other expressions in places where multiple parameters or elements are expected.

The ES5 code below uses apply() to compute the maximum value in an array:
```
var arr = [6, 89, 3, 45];
var maximus = Math.max.apply(null, arr); // returns 89
```
We had to use Math.max.apply(null, arr) because Math.max(arr) returns NaN. Math.max() expects comma-separated arguments, but not an array. The spread operator makes this syntax much better to read and maintain.

```
const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr); // returns 89
```

`...arr` returns an unpacked array. In other words, it spreads the array
However, the spread operator only works in-place, like in an argument to a function or in an array literal. 

## Destructuring Assignment

Destructuring assignment is special syntax introduced in ES6, for neatly assigning values taken directly from an object.

The following ES5 code 
```
const user = { name: 'John Doe', age: 34 };

const name = user.name; // name = 'John Doe'
const age = user.age; // age = 34

```

can be reduced to 

```
const { name, age } = user;
```

Here, the name and age variables will be created and assigned the values of their respective values from the user object.

Destructuring allows you to assign a new variable name when extracting values. You can do this by putting the new name after a colon when assigning the value.
Here's how you can give new variable names in the assignment:
```
const { name: userName, age: userAge } = user;
```
We can use the same principles to destructure values from a nested objects.

Example
```
const user = {
  johnDoe: { 
    age: 34,
    email: 'johnDoe@freeCodeCamp.com'
  }
};
```

```
const { johnDoe: { age: userAge, email: userEmail }} = user;
```

Assign variables from array.

ES6 makes destructuring arrays as easy as destructuring objects.

One key difference between the spread operator and array destructuring is that the spread operator unpacks all contents of an array into a comma-separated list. Consequently, you cannot pick or choose which elements you want to assign to variables.
Destructuring an array lets us do exactly that:

```
const [a, b] = [1, 2, 3, 4, 5, 6];
console.log(a, b); // 1, 2
```
The variable a is assigned the first value of the array, and b is assigned the second value of the array. We can also access the value at any index in an array with destructuring by using commas to reach the desired index:

```
const [a, b,,, c] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c); // 1, 2, 5
```

Swapping values
```
let a = 8, b = 6;
 [b,a] =[a,b];
```


