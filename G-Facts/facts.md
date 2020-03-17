----
> Name : Syed Modassir Ali
> Date : 18.03.2020
> Title : Facts
----

# Fact 1

In C language, sizeof( ) is an operator. Though it looks like a function, it is an unary operator.

For example in the following program, when we pass a++ to sizeof, the expression “a++” is not evaluated. However in case of functions, parameters are first evaluated, then passed to function.

```cpp
// C program to demonstrate that sizeof 
// is an operator 
#include<stdio.h> 

int main() 
{ 
	int a = 5; 
	printf("%d\n", sizeof(++a)); 
	printf("%d", a); 
	return 0; 
} 
```
OUTPUT:
```
4
5
```

# Fact 2
