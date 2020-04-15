----
> Name  : Syed Modassir Ali
> Date  : 30.03.2020
> Title : Javascript (VanillaJS)
----

# Introduction

JavaScript is a high-level programming language that all modern web browsers support. It is also one of the core technologies of the web

## Comments

Comments helps us make the code easily readable and understoodable by developers.

`// This is a single line comment`

```
/*
* Multi Line comment
*/
```

## Data Types

JavaScript provides 7 different data types undefined, null, boolean, string, symbol, number, and object.
Variables are container address names used to store values.
In JavaScript, we can store a value in a variable using the assignment operator. 
```
var ourVariable = 10;
```

**ECMAS added support for let, const keyword which we shall look later.**

Undefined variables cant be used for operations. Variable names are case sensitive. We generally use camelcase as variable names.
JavaScript variables undergoes mathematical operations like regular variables.
We can use escape sequences or double quoted texts inside single quotes.

## Input and Output

`alert()` gives an alert prompt on the browser.
`console.log()` gives the output on the developers console and 
`document.Write()` gives output inside the webpage

`document.getElementById("id").innerHTML=` to modify inner contents inside of HTML tags

`prompt()` is used to get user input through prompt.
`document.getElementById("id").value` to get values from form inputs.

## Boolean

Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.

use `arr.filter(Boolean);`  to remove them.

## Strings

Strings are treated as character array in JavaScript. `.length` is used to calculate the length of an array.
In JavaScript, String values are immutable, which means that they cannot be altered once created. 

`.split("")`  splits the string based on the arguments passed.   `.reverse()` reverses the array.    `.join("")` joins the array back using the argument passed.

`let a =Math.max(...str.split(" ").map(word => word.length));` to find the word in an array having maximum length.

`.endsWith()` determines if a particular string ends with a particular substring.


## Arrays

`var myArray = ["Item1",Number1,.....]`

We can create array of arrays to create multidimensional arrays.
Unlike Strings Arrays are mutable.
Data can be added to the end of the array using the `.push()` function.

```
var myArray = [1,2,3];
myArray.push(4);
// myArray = [1,2,3,4];
```

`.pop()` function is used to remove an element from the end of the array.

```
var myArray = [1,2,3];
var popped = myArray.pop();
// myArray = [1,2];
```

`.shift()` function removes element from the first.

`.unshift()` works like push function adds element to the first.

```
JSON.stringify(); // converts array to string
```

## Objects

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


JSON(JavaScript Object Notation) is a related data interchange format used to store data.
 
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
----

## Conditonal Statements

```
if(Condition1)
{
	// code to execute
}
else if(condition2)
{
	// code to execute
}
else
{
	// code to execute
}
```

### Comparision Operator
In conditionals there is a difference between equality and strict equality.
`===` and `==`
`!==` and `!=`

Logical AND `&&` OR `||`

### Ternary

`condition ? statement-if-true : statement-if-false;`


## Switch Case

There can be multiple datatypes for cases

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

## Loops

### While Loop

```
while(condition){
  // body of the loop 
}
```

### for loop

```
for ([initialization]; [condition]; [final-expression])
```

### Nested Loops

### do-While loops

```
do
{
  //body of the loop
}while(condition);
```


## Functions

In JavaScript, we can divide up our code into reusable parts called functions.

```
function functionName(){
	// Body of the function 
}
```

or

```
function functionName(param1,param2) {
  console.log("Hello World");
}
```

There are two parts creating the function and calling the function.
Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.


### Variable Scope
 
Scope of variable is also important. Variables which are used without the var keyword are automatically created in the global scope. 
Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

Boolean data types true / false.

### Arrow function

In JavaScript, we often don't need to name our functions, especially when passing a function as an argument to another function. 
Instead, we create inline functions. We don't need to name these functions because we do not reuse them anywhere else.

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

`const myFunc = () => "value";`

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

## Recursion

```
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```
## Some Functions

`Math.random();`     `Math.floor();`
`Math.floor(Math.random() * (max - min + 1)) + min`

Use `parseInt()` in the convertToInteger function so it converts the input string str into an integer, and returns it.

`parseInt(string, radix);`

`radix` accepts values between 2 to 36.

## Functional Programming

We will review this section later.


-----
-----

# ES6

ECMAScript is a standardized version of JavaScript with the goal of unifying the language's specifications and features. 
As all major browsers and JavaScript-runtimes follow this specification, the term ECMAScript is interchangeable with the term JavaScript.

## Variable declaration

`let` keyword helps us create a vraibale within the local scope and also helps us avoid multiple variable declaration.

`const` has all the awesome features that let has, with the added bonus that variables declared using const are read-only. 
They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned.

**Common convention is to name const variables with ALL CAPS.**
**Constructors are named with their names starting in uppercase.**


### Mutation
Objects (including arrays and functions) assigned to a variable using const are still mutable.
To ensure your data doesn't change, JavaScript provides a function `Object.freeze` to prevent data mutation.
Once the object is frozen, you can no longer add, update, or delete properties from it. Any attempt at changing the object will be rejected without an error.


## Arrow Function 

( Completed under functions seciton)

## Rest parameter and Spread operator

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

The ES5 code below uses `apply()` to compute the maximum value in an array:
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

### Basics

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

### Assigning new variables using Destructuring

Destructuring allows you to assign a new variable name when extracting values. You can do this by putting the new name after a colon when assigning the value.
Here's how you can give new variable names in the assignment:
```
const { name: userName, age: userAge } = user;
```

### Nested Objects

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

### Assign variables from array

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

`Array.prototype.slice()`
 

**Using destructuring assignment with the rest parameter to perform an effective `Array.prototype.slice()` so that arr is a sub-array of the original array source with the first two elements omitted.**


### Destructure the object in a function argument itself.

```
const profileUpdate = (profileData) => {
  const { name, age, nationality, location } = profileData;
}
```

This effectively destructures the object sent into the function. This can also be done in-place:

```
const profileUpdate = ({ name, age, nationality, location }) => {
// code to execute with these fields.
}
```

This removes some extra lines and makes our code look neat. This has the added benefit of not having to manipulate an entire object in a function —
 only the fields that are needed are copied inside the function.

It also helps during API calls.

## Template literal

A new feature of ES6 is the template literal. This is a special type of string that makes creating complex strings easier.
Template literals allow you to create multi-line strings and to use string interpolation features to create strings.

```
const person = {
  name: "Zodiac Hasbro",
  age: 56
};

// Template literal with multi-line and string interpolation
const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

console.log(greeting); // prints
// Hello, my name is Zodiac Hasbro!
// I am 56 years old.
```

A lot of things happened there. Firstly, the example uses backticks ( \` ), not quotes (' or "), to wrap the string. Secondly, notice that the string is multi-line, both in the code and the output. This saves inserting \n within strings. The ${variable} syntax used above is a placeholder. Basically, you won't have to use concatenation with the + operator anymore. To add variables to strings, you just drop the variable in a template string and wrap it with ${ and }. Similarly, you can include other expressions in your string literal, for example ${a + b}. This new way of creating strings gives you more flexibility to create robust strings.

## Object Literal

Write Concise Object Literal Declarations Using Object Property Shorthand
ES6 adds some nice support for easily defining object literals.

Consider the code:
```
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});
```

This can be reduced to:
```
const getMousePosition = (x, y) => ({ x, y });
```

## Functions inside Objects

Write Concise Declarative Functions with ES6

When defining functions within objects in ES5, we have to use the keyword function as:

```
const person = {
  name: "Taylor",
  sayHello: function() {
    return `Hello! My name is ${this.name}.`;
  }
};
```
With ES6, You can remove the function keyword and colon altogether when defining functions in objects. Here's an example of this syntax:

```
const person = {
  name: "Taylor",
  sayHello() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

## Constructors and Object Creation

We will see this in the Object Oriented Programming section. Just creation Syntax here.

## Getters and Setters

Use getters and setters to Control Access to an Objects private data.
We can obtain values from an object and set the value of a property within an object using the getters and setters.
Getter functions are meant to simply return (get) the value of an object's private variable to the user without the user directly accessing the private variable.

Setter functions are meant to modify (set) the value of an object's private variable based on the value passed into the setter function. 
This change could involve calculations, or even overwriting the previous value completely.

```
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer() {
    return this._author;
  }
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
const lol = new Book('anonymous');
console.log(lol.writer);  // anonymous
lol.writer = 'wut';
console.log(lol.writer);  // wut
```

**Notice the syntax used to invoke the getter and setter. They do not even look like functions. Getters and setters are important because they hide internal implementation details. Note: It is convention to precede the name of a private variable with an underscore (_).**

## Modules, Import and Export

In order to make JavaScript more modular, clean, and maintainable; ES6 introduced a way to easily share code among JavaScript files. 
This involves exporting parts of a file for use in one or more other files, and importing the parts you need, where you need them. 
In order to take advantage of this functionality, we need to create a script in your HTML document with a type of module.

`<script type="module" src="index.js"></script>`  index.js file will import the features 


A script that uses this module type can now use the import and export features.
```
export const add = (x, y) => {
  return x + y;
}
```

```
const add = (x, y) => {
  return x + y;
}

export { add };
```

import allows you to choose which parts of a file or module to load. 
`import { add } from "./math_functions.js";`

default export
` export default { add }`

default import
` import add from "./maths_function.js"`

default imports can be named anything

import all
`import * as somefunction from "./maths_function.js"`

## Promise

A promise in JavaScript is exactly what it sounds like - you use it to make a promise to do something, usually asynchronously. 
When the task completes, you either fulfill your promise or fail to do so. 
Promise is a constructor function, so you need to use the new keyword to create one. 
It takes a function, as its argument, with two parameters - resolve and reject. These are methods used to determine the outcome of the promise. 

A promise has three states: pending, fulfilled, and rejected. 
The promise without any condition is forever stuck in the pending state because you did not add a way to complete the promise. 
The resolve and reject parameters given to the promise argument are used to do this. 
resolve is used when you want your promise to succeed, and reject is used when you want it to fail. These are methods that take an argument, as seen below.

```
const myPromise = new Promise((resolve, reject) => {
  if(condition here) {
    resolve("Promise was fulfilled");
  } else {
    reject("Promise was rejected");
  }
});
```

**Make Server Request problem.**

```
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer represents a response from a server
  let responseFromServer;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

```

Promises are most useful when you have a process that takes an unknown amount of time in your code (i.e. something asynchronous), often a server request. When you make a server request it takes some amount of time, and after it completes you usually want to do something with the response from the server. 
This can be achieved by using the then method. The then method is executed immediately after your promise is fulfilled with resolve. Here’s an example:

```
myPromise.then(result => {
  // do something with the result.
	console.log(result);
});
```

catch is the method used when your promise has been rejected. It is executed immediately after a promise's reject method is called. Here’s the syntax:

```
myPromise.catch(error => {
  // do something with the error.
	console.log(error);
});
```
error is the argument passed in to the reject method.

**Simple example of a promise**
```
const p = new Promise((resolve, reject)=>{
	let flag;
	if(flag)
	{
		resolve("SUCCESS");
	}
	else
	{
		reject("FAILURE");
	}
});

p.then(message=>{
	console.log(message);
}).catch(message =>{ 
	console.log(message);
});
```

`Promise.all()` and `Promise.race()`

## Callbacks

callbacks are similar to promises

----

# Regular Expression

Regular expressions are special strings that represent a search pattern.
Also known as "regex" or "regexp", they help programmers match, search, and replace text. 
Regular expressions can appear cryptic because a few characters have special meaning. 
The goal is to combine the symbols and text into a pattern that matches what you want, but only what you want. 
This section will cover the characters, a few shortcuts, and the common uses for writing regular expressions.

## Test method

Regular expressions are used in programming languages to match parts of strings. You create patterns to help you do that matching.
If you want to find the word "the" in the string "The dog chased the cat", you could use the following regular expression: /the/. 
Notice that quote marks are not required within the regular expression.
JavaScript has multiple ways to use regexes. One way to test a regex is using the .test() method. The .test() method takes the regex, 
applies it to a string (which is placed inside the parentheses), and returns true or false if your pattern finds something or not.

```
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr);
// Returns true
```
The test function matches the regex when the case matches.

## Match multiple words

We can search for multiple patterns using the alternation or OR operator: |.
This operator matches patterns either before or after it. For example, if you wanted to match "yes" or "no", the regex you want is /yes|no/.
You can also search for more than just two patterns. You can do this by adding more patterns with more OR operators separating them, like /yes|no|maybe/.

```
let petRegex = /dog|cat|bird|fish/; 
```

## Ignore Case While Matching

There are other flags but here we'll focus on the flag that ignores case - the i flag. 
We can use it by appending it to the regex. An example of using this flag is /ignorecase/i. 
This regex can match the strings "ignorecase", "igNoreCase", and "IgnoreCase".

`let fccRegex = /freecodecamp/i;`

## Extract Matches

We can also extract the actual matches you found with the `.match()` method.
To use the `.match()` method, apply the method on a string and pass in the regex inside the parentheses. 
Here's an example:

```
"Hello, World!".match(/Hello/);
// Returns ["Hello"]
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
// Returns ["expressions"]
```

It returns the regex, index and the input string.

## More than one match

To search or extract a pattern more than once, you can use the g flag.

```
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
```

## Match Anything with Wildcard Period

The wildcard character . will match any one character. The wildcard is also called dot and period. 
We can use the wildcard character just like any other character in the regex. 
For example, if we wanted to match "hug", "huh", "hut", and "hum", you can use the regex /hu./ to match all four words.

`let repeatRegex = /.un/`

## Match Single Character with Multiple Possibilities

We learned how to match literal patterns (/literal/) and wildcard character (/./). 
Those are the extremes of regular expressions, where one finds exact matches and the other matches everything. 
There are options that are a balance between the two extremes.
We can search for a literal pattern with some flexibility with `character classes`. 
Character classes allow you to define a group of characters you wish to match by placing them inside square ([ and ]) brackets.
For example, you want to match "bag", "big", and "bug" but not "bog". We can create the regex /b[aiu]g/ to do this. 
The [aiu] is the character class that will only match the characters "a", "i", or "u".

```
let quoteSample = "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /[aeiou]/ig; // Change this line
let result = quoteSample.match(vowelRegex); // Change this line
console.log(result);
```

## Match Letters of the Alphabet

We saw how we can use character sets to specify a group of characters to match, 
but that's a lot of typing when you need to match a large range of characters (for example, every letter in the alphabet). 
Fortunately, there is a built-in feature that makes this short and simple.
Inside a character set, we can define a range of characters to match using a hyphen character: -.
For example, to match lowercase letters a through e you would use [a-e].

```
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /[a-z]/ig; // Change this line
let result = quoteSample.match(alphabetRegex); // Change this line
console.log(result);
```

## Match Numbers and Letters of the Alphabet

Using the hyphen (-) to match a range of characters is not limited to letters. It also works to match a range of numbers.
For example, /[0-5]/ matches any number between 0 and 5, including the 0 and 5.
Also, it is possible to combine a range of letters and numbers in a single character set.

```
let jennyStr = "Jenny8675309";
let myRegex = /[a-z0-9]/ig;
// matches all letters and numbers in jennyStr
jennyStr.match(myRegex);
```

## Match Single Characters Not Specified

So far, we have created a set of characters that we want to match, but we could also create a set of characters that we do not want to match. 
These types of character sets are called negated character sets. To create a negated character set, 
we place a caret character (^) after the opening bracket and before the characters we do not want to match.
For example, /[^aeiou]/gi matches all characters that are not a vowel. Note that characters like ., !, [, @, / and white space are matched - 
the negated vowel character set only excludes the vowel characters.

```
let quoteSample = "3 blind mice.";
let myRegex = /[^0-9aeiou]/ig; 
let result = quoteSample.match(myRegex); 
console.log(result);
```

## Match Characters that Occur One or More Times

Sometimes, we need to match a character (or group of characters) that appears one or more times in a row. 
This means it occurs at least once, and may be repeated.
We can use the + character to check if that is the case. Remember, the character or pattern has to be present consecutively. 
That is, the character has to repeat one after the other.
For example, /a+/g would find one match in "abc" and return ["a"]. Because of the +, it would also find a single match in "aabc" and return ["aa"].

## Match Characters that Occur Zero or More Times

The character to do this is the asterisk or star: *.

## Find Characters with Lazy Matching

Regular expressions are by default greedy, so the match would return ["titani"]. It finds the largest sub-string possible to fit the pattern.
However, we can use the ? character to change it to lazy matching. "titanic" matched against the adjusted regex of /t[a-z]*?i/ returns ["ti"].

## Match Beginning String Patterns

Outside of a character set, the caret is used to search for patterns at the beginning of strings.

```
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
// Returns true
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
// Returns false
```

## Match Ending String Patterns

You can search the end of strings using the dollar sign character $ at the end of the regex.

```
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding);
// Returns true
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding);
// Returns false
```

## Match All Letters and Numbers

Use the shorthand character class \w to count the number of alphanumeric characters in various quotes and strings.

`let alphabetRegexV2 = /\w/g; `

## Match Everything But Letters and Numbers

We can search for the opposite of the \w with \W. Note, the opposite pattern uses a capital letter. This shortcut is the same as [^A-Za-z0-9_].

## Match All Number and non Numbers

We can use \d to match all numbers in a regex. \D is used for non numbers.

## Match with variables

We can use a constructor to create a re using a variable each time the variable is modified.
`let re = new RegExp(target + "$", "ig");`

## Username check

`let userCheck = /^[a-z]([0-9]{2,}|[a-z]+\d*)$/i;`

## Whitespaces and non whitespaces

Whitespaces are checked using \s . Search for non-whitespace using \S, which is an uppercase s. 
This pattern will not match whitespace, carriage return, tab, form feed, and new line characters. 
We can think of it being similar to the character class [^ \r\t\f\n\v].

## Specify Upper and Lower Number of Matches

We can specify the lower and upper number of patterns with quantity specifiers. 
Quantity specifiers are used with curly brackets ({ and }). We put two numbers between the curly brackets - for the lower and upper number of patterns.
For example, to match only the letter a appearing between 3 and 5 times in the string "ah", your regex would be /a{3,5}h/.

`/a{n}/` denotes n a's and `/a{n,}/` denotes minimum n a's.

## Check for all or none

We can specify the possible existence of an element with a question mark, ?. This checks for zero or one of the preceding element.

`/u?/` denotes 0 or 1 u's

## Positive and Negative Lookahead

Lookaheads are patterns that tell JavaScript to look-ahead in your string to check for patterns further along. 
This can be useful when we want to search for multiple patterns over the same string.
There are two kinds of lookaheads: positive lookahead and negative lookahead.
A positive lookahead will look to make sure the element in the search pattern is there, but won't actually match it. 
A positive lookahead is used as `(?=...)` where the `...` is the required part that is not matched.
On the other hand, a negative lookahead will look to make sure the element in the search pattern is not there. 
A negative lookahead is used as `(?!...)` where the `...` is the pattern that you do not want to be there. 
The rest of the pattern is returned if the negative lookahead part is not present.

Question : Use lookaheads in the pwRegex to match passwords that are greater than 5 characters long, do not begin with numbers, and have two consecutive digits.
```
let sampleWord = "astronaut";
let pwRegex = /^\D(?=\w{5})(?=\w*\d{2})/;
let result = pwRegex.test(sampleWord);
```

## Check For Mixed Grouping of Characters

Sometimes we want to check for groups of characters using a Regular Expression and to achieve that we use parentheses ().
If we want to find either Penguin or Pumpkin in a string, we can use the following Regular Expression: /P(engu|umpk)in/g
Then check whether the desired string groups are in the test string by using the test() method.

```
let testStr = "Pumpkin";
let testRegex = /P(engu|umpk)in/;
testRegex.test(testStr);
```

## Use Capture Groups to Search and Replace

We can search and replace text in a string using `.replace()`  on a string. The inputs for `.replace()` is first the regex pattern we want to search for. 
The second parameter is the string to replace the match or a function to do something.

```
let wrongText = "The sky is silver.";
let silverRegex = /silver/;
wrongText.replace(silverRegex, "blue");
// Returns "The sky is blue."
```

We can also access capture groups in the replacement string with dollar signs ($).

```
"Code Camp".replace(/(\w+)\s(\w+)/, '$2 $1');
// Returns "Camp Code"
```

## Remove Whitespace from Start and End

`String.prototype.trim()` works fine but we shall use regex here.

```
let hello = "   Hello, World!  ";
let wsRegex = /^\s+|\s+$/g;
let result = hello.replace(wsRegex, ""); 
console.log(result);
```


----


# Debugging

Debugging is a valuable and (unfortunately) necessary tool for programmers. 
It follows the testing phase of checking if your code works as intended, and discovering it does not. 
Debugging is the process of finding exactly what isn't working and fixing it. 
After spending time creating a brilliant block of code, it is tough realizing it may have errors. These issues generally come in three forms:

   - syntax errors that prevent a program from running
   - runtime errors when code fails to execute or has unexpected behavior
   - semantic (or logical) errors when code doesn't do what it's meant to.


## Display variable values
Use console.log() to display value of variables.
console.clear() to clear the console.

## Type of to check variable type
console.log(typeof variable);
----
----

# DOM Manipulation 

## Selecting and Changing website elements.

`document.getElementByID()` to select elements of a particular ID. 
`document.getElementsByClassName()`  to select elemnets of particular classes.
`div1.getElementsByClassName()`  to select elements of a particular class inside div1 container.
`document.getElementByTagName()` to select elements based on HTML tags.
`document.querySelector()` to find the first element with this query
`document.querySelectorAll()` to find and select all queries.
`.innerHTML` to change inner contents of a HTML.  // This can create a XSS attack
`.textContent` to parse inner contents as text rather than HTML.

## Setting and Getting Css Styles.

`.style.color` to change the text color
`.style.background` to change the background color
`.style.boxShadow` to change the box shadow property.
`.style.cssText` to set multiple styles.
`.setAttribute()` to put multiple styles. // both cssText and setAttributes overrides the inline styling.
`window.getComputedStyle()` to show all styles pre-computed.

## Events

`.onclick` when an element is clicked
`.oninput` when an input is provided
`.onload` when page is loaded
`.onmouseover` when mouse is over an element
`.onmouseout` when mouse is over an element and moves out.
`resize`

## Event Listner

`element.addEventListener(event, function, useCapture)`
`element.removeEventListner(event, function, useCapture)` //Parameters must be same

## Nodes

`.appendChild()`
`.replaceChild()`
`.removeChild()`

## Animation in DOM

`element.animate(keyframes as objects array, options as object)`

## Request Animation Frame

`window.requestAnimationFrame()` //gives a stop id. used with callbacks generally
`cancelAnimationFrame(stopId)`

## Window Objects

This represents the browser window. 
`.innerWidth` `.innerHeight`
`.open()` `.close()` `.moveBy()` `.moveTo()` `.focus()`

## Pop up Boxes

`alert()` `confirm("Message")` `prompt("Message", default value)`

## Cookies, local and session storage

Cookies store 4kb data. Local Storage 10mb and Session Storage 5mb. Session storage are accessible from the same tab that was used to create it.
Cookies are stored on browser and server and sent to the server with request.

`localStorage.setItem(key,value)` `sessionStorage.setItem(key,value)`
`.removeItem()` `.clear()`   `document.cookie = "key=value; expires=date-time";path=/;` path here signifies the path to which the cookie is associated.

To delete a cookie set the cookie to have an expired expiration date(01 Jan 1970 00:00:00 UTC;) but same path and value as blank.

## History

`.history` `window.history.length` `history.back()` `history.forward()` `history.go(n)` 
`history.replaceState(Json object, name, website)` `history.state` `history.pushState(state or json object, name, url )`

`turn_off_js=true;`

----
----
# Data Structures

In Computer Science a queue is an abstract Data Structure where items are kept in order. 
New items can be added at the back of the queue and old items are taken off from the front of the queue.
Queue. (LIFO)

## Array

## Basic Insertion and deletion
We can pop() push() shift() unshift() in an array.

## Higher order Array Functions

### .splice()
`splice()` allows us to remove any number of consecutive elements from anywhere in an array.
splice() can take up to 3 parameters, but for now, we'll focus on just the first 2. The first two parameters of splice() are integers which represent indexes, 
or positions, of the array that splice() is being called upon. And remember, arrays are zero-indexed, so to indicate the first element of an array, 
we would use 0. splice()'s first parameter represents the index on the array from which to begin removing elements, 
while the second parameter indicates the number of elements to delete. 

`splice()` can take up to three parameters. Well, we can use the third parameter, comprised of one or more element(s), to add to the array. 
This can be incredibly useful for quickly switching out an element, or a set of elements, for another.

```
const numbers = [10, 11, 12, 12, 15];
const startIndex = 3;
const amountToDelete = 1;

numbers.splice(startIndex, amountToDelete, 13, 14);
// the second entry of 12 is removed, and we add 13 and 14 at the same index
console.log(numbers);
// returns [ 10, 11, 12, 13, 14, 15 ]
```

### .slice()
`.slice()`, rather than modifying an array, copies, or extracts, a given number of elements to a new array, 
leaving the array it is called upon untouched. `.slice()` takes only 2 parameters — the first is the index at which to begin extraction, 
and the second is the index at which to stop extraction.

### .indexOf()
`.indexOf()` returns the index of an item if present in the array else returns -1.

### every()

`array.every(condition)` returns true if every item present in an array satisfies the given condition.

### some()

`array.some(condition)` returns true or false for an item present in the array

### forEach

`array.forEach(function(parameter in the array){ condition });` checks the condition for each item in the array.

### filter

Return filtered items from an array.
`array.filter(function(array){ condition? true : false })`

### map

Create array of items from array passed based on condition.
`array.map(array=> condition? return a : return b ; )`

### sort

`array.sort((a,b)=> a - b;)` return 1 or -1

### reduce

To add all the items
`array.reduce((total,array)=> total+age , 0)` reduces the array to a single value.

### Access object key value pairs and change them.

This has been dealt under the objects and OOP section.

### iterating key inside an object

```
for (let user in usersObj) {
    if (usersObj[user].online === true) {
      result++;
    }
```

### Generating and array of object keys

We can also generate an array which contains all the keys stored in an object using the `Object.keys()` method and passing in an object as the argument. 
This will return an array with strings representing each property in the object. Again, there will be no specific order to the entries in the array.

```
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function getArrayOfUsers(obj) {
    return Object.keys(obj);
  }
console.log(getArrayOfUsers(users));
```

### Updating an array inside of an object and then returning it.

```
function addFriend(userObj, friend) {
  userObj.data.friends.push(friend);
  return userObj.data.friends;
}
```

----
----

# Object Oriented Programming

## Introduction
At its core, software development solves a problem or achieves a result with computation. The software development process first defines a problem, then presents a solution. Object oriented programming is one of several major approaches to the software development process.

As its name implies, object oriented programming organizes code into object definitions. These are sometimes called classes, and they group together data with related behavior. The data is an object's attributes, and the behavior (or functions) are methods.

The object structure makes it flexible within a program. Objects can transfer information by calling and passing data to another object's methods. Also, new classes can receive, or inherit, all the features from a base or parent class. This helps to reduce repeated code.

Your choice of programming approach depends on a few factors. These include the type of problem, as well as how you want to structure your data and algorithms.

## Creating an Object

```js
let obj = {
	key : value,
	// more key value pairs,
	key : value
};
```

## Creating a function inside an object

```js
let obj = {
	objectfucntion(){
		// body of the function	
	}
};
```

## Using dot notation to access object properties

A property such as `eat` under `Animals` object can be accessed as `Animals.eat`

## Make code reusable using the this keyword

`this` keyword is used to access the objects property already created.

## Using constructor to create new objects

Constructors are functions that create new objects. They define properties and behaviors that will belong to the new object. 

```
function Object() {
  this.key1 = value1;
  this.key2 = value2;
  this.key3 = value3;
}

let newOBject = new Object();
```
the new operator is used when calling a constructor. This tells JavaScript to create a new instance of Object called newObject. 
Without the new operator, this inside the constructor would not point to the newly created object, giving unexpected results.

## Constructor and Object creation

**Use class Syntax to Define a Constructor Function**

ES6 provides a new syntax to create objects, using the class keyword.

It should be noted that the class syntax is just syntax, and not a full-fledged class-based implementation of an object-oriented paradigm, unlike in languages such as Java, Python, Ruby, etc.

In ES5, we usually define a constructor function and use the new keyword to instantiate an object.

```
var SpaceShuttle = function(targetPlanet){
  this.targetPlanet = targetPlanet;
}
var zeus = new SpaceShuttle('Jupiter');
```

The class syntax simply replaces the constructor function creation:

```
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
}
const zeus = new SpaceShuttle('Jupiter');
```
It should be noted that the class keyword declares a new function, to which a constructor is added. This constructor is invoked when new is called to create a new object.

## Verify an Object's Constructor with instanceof

Anytime a constructor function creates a new object, that object is said to be an instance of its constructor. 
JavaScript gives a convenient way to verify this with the `instanceof` operator. 
`instanceof` allows us to compare an object to a constructor, returning true or false based on whether or not that object was created with the constructor.

## Check if an object has a particular property

`.hasOwnProperty()`

## Use Prototype Properties to Reduce Duplicate Code

`Bird.prototype.numLegs = 2;`

## Understand the Constructor Property

`constructor` property is a reference to the constructor function that created the instance

## Change the Prototype to a New Object

A more efficient way is to set the prototype to a new object that already contains the properties. This way, the properties are added all at once.

```
Bird.prototype = {
  numLegs: 2, 
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name);
  }
};
```

```
Dog.prototype = {
  numLegs : 4,
  eat(){

  },
  describe(){

  }
};
```

## Remember to Set the Constructor Property when Changing the Prototype

There is one crucial side effect of manually setting the prototype to a new object. It erases the constructor property! 
This property can be used to check which constructor function created the instance, but since the property has been overwritten, 
it now gives false results.

```
Bird.prototype = {
  constructor: Bird, // define the constructor property
  numLegs: 2,
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name); 
  }
};
```

## Understand Where an Object’s Prototype Comes From

Just like people inherit genes from their parents, an object inherits its prototype directly from the constructor function that created it. 

`Bird.prototype.isPrototypeOf(duck);` to check if duck inherits its prototype from Bird.

## Understanding the prototype chain

`Object.prototype.isPrototypeOf(Dog.prototype);`









## Use Inheritance So You Don't Repeat Yourself(DRY)

```
Bird.prototype = {
  constructor: Bird,
  describe: function() {
    console.log("My name is " + this.name);
  }
};

Dog.prototype = {
  constructor: Dog,
  describe: function() {
    console.log("My name is " + this.name);
  }
};
```

The describe method is repeated in two places. The code can be edited to follow the DRY principle by creating a supertype (or parent) called Animal:

```
function Animal() { };

Animal.prototype = {
  constructor: Animal, 
  describe: function() {
    console.log("My name is " + this.name);
  }
};
```

Since Animal includes the describe method, you can remove it from Bird and Dog:

```
Bird.prototype = {
  constructor: Bird
};

Dog.prototype = {
  constructor: Dog
};
```
## Inherit Behaviors from a Supertype

Reuse Animal's methods inside Bird and Dog without defining them again. It uses a technique called inheritance. 
This challenge covers the first step: make an instance of the supertype (or parent). We already know one way to create an instance of Animal using the new operator:

`let animal = new Animal();`

There are some disadvantages when using this syntax for inheritance, which are too complex for the scope of this challenge. 
Instead, here's an alternative approach without those disadvantages:

`let animal = Object.create(Animal.prototype);`

`Object.create(obj)` creates a new object, and sets obj as the new object's prototype. 
Recall that the prototype is like the "recipe" for creating an object. 
By setting the prototype of animal to be Animal's prototype, you are effectively giving the animal instance the same "recipe" as any other instance of Animal.

```
animal.eat(); // prints "nom nom nom"
animal instanceof Animal; // => true
```

## Set the Child's Prototype to an Instance of the Parent

set the prototype of the subtype (or child)—in this case, Bird—to be an instance of Animal.

`Bird.prototype = Object.create(Animal.prototype);`

Remember that the prototype is like the "recipe" for creating an object. In a way, the recipe for Bird now includes all the key "ingredients" from Animal.

## Reset an Inherited Constructor Property

When an object inherits its prototype from another object, it also inherits the supertype's constructor property.

```
function Bird() { }
Bird.prototype = Object.create(Animal.prototype);
let duck = new Bird();
duck.constructor // function Animal(){...}
```

But duck and all instances of Bird should show that they were constructed by Bird and not Animal. 
To do so, we can manually set Bird's constructor property to the Bird object.

```
Bird.prototype.constructor = Bird;
duck.constructor // function Bird(){...}
```

## Add Methods After Inheritance

A constructor function that inherits its prototype object from a supertype constructor function can still have its own methods in addition to inherited methods.

```
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };

function Dog() { }

Dog.prototype= Object.create(Animal.prototype);
Dog.prototype.constructor= Dog;
Dog.prototype.bark=function(){
  console.log("Woff!");
}
let beagle = new Dog();

```

## Override Inherited Methods

`ChildObject.prototype = Object.create(ParentObject.prototype);` 
Then the ChildObject received its own methods by chaining them onto its prototype.

`ChildObject.prototype.methodName = function() {...};`
It's possible to override an inherited method. It's done the same way - by adding a method to ChildObject.prototype using the same method name as the one to override.

```
function Animal() { }
Animal.prototype.eat = function() {
  return "nom nom nom";
};
function Bird() { }

// Inherit all methods from Animal
Bird.prototype = Object.create(Animal.prototype);

// Bird.eat() overrides Animal.eat()
Bird.prototype.eat = function() {
  return "peck peck peck";
};
```

If you have an instance let duck = new Bird(); and you call duck.eat(), this is how JavaScript looks for the method on duck’s prototype chain:

   - duck => Is eat() defined here? No.
   - Bird => Is eat() defined here? => Yes. Execute it and stop searching.
   - Animal => eat() is also defined, but JavaScript stopped searching before reaching this level.
   - Object => JavaScript stopped searching before reaching this level.

## Use a Mixin to Add Common Behavior Between Unrelated Objects

As we have seen, behavior is shared through inheritance. However, there are cases when inheritance is not the best solution. 
Inheritance does not work well for unrelated objects like Bird and Airplane. They can both fly, but a Bird is not a type of Airplane and vice versa.
For unrelated objects, it's better to use mixins. A mixin allows other objects to use a collection of functions.

```
let flyMixin = function(obj) {
  obj.fly = function() {
    console.log("Flying, wooosh!");
  }
};
```

The flyMixin takes any object and gives it the fly method.

## Use Closure to Protect Properties Within an Object from Being Modified Externally

In JavaScript variables declared outside are automatically available within the function. JS uses lexical scoping i.e inner function variables are not accessible outside but outer variables can be accessed inside.
```
var addTo = function(passed){
	var add = function(inner){
		return passed+inner;
	};
	return add;
};

```

## Understand the Immediately Invoked Function Expression (IIFE)

A common pattern in JavaScript is to execute a function as soon as it is declared.

```
(function () {
  console.log("Chirp, chirp!");
})();
```
Note that the function has no name and is not stored in a variable. 
The two parentheses () at the end of the function expression cause it to be immediately executed or invoked. 
This pattern is known as an immediately invoked function expression or IIFE.


## Use an IIFE to Create a Module

An immediately invoked function expression (IIFE) is often used to group related functionality into a single object or module. 

```
function glideMixin(obj) {
  obj.glide = function() {
    console.log("Gliding on the water");
  };
}
function flyMixin(obj) {
  obj.fly = function() {
    console.log("Flying, wooosh!");
  };
}
```

We can group these mixins into a module as follows:

```
let motionModule = (function () {
  return {
    glideMixin: function(obj) {
      obj.glide = function() {console.log("Gliding on the water");};
    },
    flyMixin: function(obj) {
      obj.fly = function() {
        console.log("Flying, wooosh!");
      };
    }
  }
})(); // The two parentheses cause the function to be immediately invoked
```

Note that we have an immediately invoked function expression (IIFE) that returns an object motionModule. 
This returned object contains all of the mixin behaviors as properties of the object. 
The advantage of the module pattern is that all of the motion behaviors can be packaged into a single object that can then be used by other parts of your code.

```
motionModule.glideMixin(duck);
duck.glide();
```

Solution FunModule
```

let funModule = (function(){
  return{
    isCuteMixin : function(obj) {
  obj.isCute = function() {
    return true;
  };
},
  singMixin : function(obj) {
  obj.sing = function() {
    console.log("Singing to an awesome tune");
  };
}
  }
})();
```

----
----

# Functional Programming







