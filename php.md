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
	...
	case N:
	default:
}
```

# GET

inside get.php
```
$_GET["stu_name"];
```

inside another html
```
<form action="get.php" type="get">
	<input type="text" name="stu_name">
</form>
```

`isset()` is used to check if a given variable set or not.

# POST

```
$_POST["username"];
$_POST["password"];
```

inside of html
```

<form action="post.php" type="post">
	<input type="text" name="username">
	<input type="password" name="password">
</form>
```

# Functions

```
function Function_name($param1,$param2){
	// body of the function
 	return $result
}
```
invoking `Function_name(arg1,arg2);`

---

# Date and Time Function

`$date = date('d/m/y');` or 
`$date = date('d.m.y');` or 
`$date = date('d-m-y');`
 
and

`$time = date('H-i-s')` or
`$time = date('H:i:s')`

# Global Variable

`global $variable-name;`

---

# Include and Require

This enables us to use the same template in different php files.
`include 'name_of_header.php' `  use relative path inside the quotes. It lets the code on the page to execute.

`require 'header.php'` works the same as include function. It doesnot let the code on the page to execute. 

# Include_once and Require_once

`include_once('header file')` or `require_once('header file')` this loads the header file only once and prevents repetition.

---

# Php Session

`die("The pade is dead")` or `exit("The page is broken")` To kill a page.

`fopen(link,directive)` to open a file or a url

```
fopen($website,'r') or exit();
```
A sessuib is a way to store informatin (in the form of variables) to be used across multiple pages. A PHP session variable is used to store information about, or change settings for a user session. Session variables hold information about one single user, and are available to all pages in the application.

Set the session.
```
session_start();
$_SESSION['key']=value;
```
To call a  session just call the session.
```
session_start();
$variable = $_SESSION['key']; 
```
Unset the session
```
session_start();
unset($_SESSION['key']); // To destroy a single session variable.
session_destroy(); // To destroy all of the session.
```

# Cookies

A cookie is used to identify a user. A cookie is a small file that the server embeds on the user's computer. Each time the same computer requests a page with the browser, it sends the cookie too.

```
//setting the cookie
//setcookie(name,value,expiry,path,domain);
//setcookie(name,value,expiry);
$time = time(); // returns a timestamp EPOCH time 1970.
$expire = $time + 100;
setcookie('student','Mark',$expire);
```

Using the cookie
```
$student = $_COOKIE['student'];
```
