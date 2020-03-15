-----
> Author : Syed Modassir Ali
> Date : 15.03.2020
-----

# Introduction

An array is a collection of items stored at contiguous memory locations. The idea is to store multiple items of the same type together. This makes it easier to calculate the position of each element by simply adding an offset to a base value, i.e., the memory location of the first element of the array

# Various Programming Languages

## C/C++
An array in C or C++ is a collection of items stored at contiguous memory locations and elements can be accessed randomly using indices of an array. They are used to store similar type of elements as in the data type must be the same for all elements. They can be used to store collection of primitive data types such as int, float, double, char, etc of any particular type. To add to it, an array in C or C++ can store derived data types such as the structures, pointers etc. 

```(Syntax)
// Array declaration by specifying size 
int arr1[10]; 

// With recent C/C++ versions, we can also declare an array of user specified size 
int n = 10; 
int arr2[n]; 

// Array declaration by initializing elements 
int arr[] = { 10, 20, 30, 40 } 

/* Compiler creates an array of size 4. above is same as "int arr[4] = {10, 20, 30, 40}" 
* Array declaration by specifying size and initializing elements 
* int arr[6] = { 10, 20, 30, 40 } 
*/

/* Compiler creates an array of size 6, initializes first 4 elements as specified by user and rest two elements as 0.
*It is same as "int arr[] = {10, 20, 30, 40, 0, 0}" 
*/```
