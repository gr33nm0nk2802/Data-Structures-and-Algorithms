----
> Name: Syed Modassir Ali
> Date: 25.04.2020
> Title: Php programming
----

# Introduction

PHP = "Hypertext Preprocessor" . It is an open-source server side scripting language. ( We can even use python)

Syntax * Php script resides between php tags which allows programmers to embed php scripts within HTML pages *

```
<?php
     echo "Hi, I'm a PHP script!";
?>	
```
It is an interpreted language hence, scripts are parsed at run-time rather than compiled beforehand. 
Source code is not visible to the client. Compatible with most databases.

Requirements : Apache(Web Server), Php and My SQL(Database)
---

To get system information from PHP
```
<?php phpinfo(); ?> 
```

Adding Comments in PHP is very easy as it supports C++ and Java style comments and also shell style comments

```
// This is C++ or Java style

# Shell style

/* C style comment */
```
---

# Variables

Variables begin with a $ sign and are case sensitive. Scope of a variable is important. Data type is dynamic.

Certain variables like Form variable ($_GET,$_POST) and server variables ($_SERVER) are reserved

Conactenation of stings is done using the period sign '.'

Escape sequences are used with \" \' etc.

---

# Conditionals

Conditional statements are similar to that in c++

Comparision and Logical operators are same.

```
$a == $b
$a === $b
$a != $b
$a <> $b
$a !== $b
$a <  $b
$a > $b
$a <= $b
$a >= $b

```

```
$a && $b or $a and $b
$a || $b or $a or $b
$a xor $b
!$a 
```

Syntax for conditional statements
```
if(condition)
{
	// body
}
else if (condition)
{
	//body
}
else
{
	//body
}
```
---

# Arrays

```
$variable = array('Mike','Jhon','Bob');
print_r($variable);
```
key position starts at 0.

## Associative array

```
$variable = array(key1 => value, key2 =>value);
print_r($variable);
```
## Multidimensional array

This is achieved by using array(array(),array(),array());

# Loops

## While loop and do-While loop

```
while(condition){
	// body of loop
}
```
and 

```
do{
	//body of loop
}while(condition);
```

## for loop

```
for(init;condition;increment){
	//body of the loop
}
```
## foreach loop

```
foreach($array as $item){
	//body of loop
}
```

# Switch Case

```
switch($variable){
	case 1:
	break;
	default:
}
```
