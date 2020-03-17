-----
> Author : Syed Modassir Ali
> Date : 15.03.2020
> Title : Array
-----

# Introduction

An array is a collection of items stored at contiguous memory locations. The idea is to store multiple items of the same type together. This makes it easier to calculate the position of each element by simply adding an offset to a base value, i.e., the memory location of the first element of the array

# Various Programming Languages

## C/C++
An array in C or C++ is a collection of items stored at contiguous memory locations and elements can be accessed randomly using indices of an array. They are used to store similar type of elements as in the data type must be the same for all elements. They can be used to store collection of primitive data types such as int, float, double, char, etc of any particular type. To add to it, an array in C or C++ can store derived data types such as the structures, pointers etc. 

```cpp
// Array declaration by specifying size 
int arr1[10]; 

// With recent C/C++ versions, we can also declare an array of user specified size 
int n = 10; 
int arr2[n]; 

// Array declaration by initializing elements 
int arr[] = { 10, 20, 30, 40 } 
 
/* Compiler creates an array of size 4. above is same as "int arr[4] = {10, 20, 30, 40}" 
* Array declaration by specifying size and initializing elements 
*/
int arr[6] = { 10, 20, 30, 40 } 

/* Compiler creates an array of size 6, initializes first 4 elements as specified by user and rest two elements as 0.
*It is same as "int arr[] = {10, 20, 30, 40, 0, 0}" 
*/
```

## Advantages of an Array in C/C++:

  - Random access of elements using array index.
  - Use of less line of code as it creates a single array of multiple elements.
  - Easy access to all the elements.
  - Traversal through the array becomes easy using a single loop.
  - Sorting is easy.

## Disadvantages of an Array in C/C++:

  - Allows a fixed number of elements to be entered which is decided at the time of declaration. Unlike a linked list, an array in C is not dynamic.
  - Insertion and deletion of elements can be costly since the elements are needed to be managed in accordance with the new memory allocation.
  
## Facts:

   - **Accessing Array Elements:** Array elements are accessed by using an integer index. Array index starts with 0 and goes till size of array minus 1.
   - **No Index Out of bound Checking:** There is no index out of bounds checking in C/C++, but may produce unexpected output when run.
   - In C, it is not compiler error to initialize an array with more elements than the specified size. However, The program won’t compile in C++. 
   - The elements are stored at contiguous memory locations
      ```
      This means if arr[0] has address 0x7ffd636b4260
      then address of arr[1] is 0x7ffd636b4264 i.e, address of arr[0] + sizeof(int) if the array stores integer data
      ```
   - A character array initialized with double quoted string has last element as ‘\0’.
   
   - In C, it is possible to have array of all types except void and functions.

  
  ### Difference between pointers and arrays in C?
  
- Pointers are used for storing address of dynamically allocated arrays and for arrays which are passed as arguments to functions. In other contexts, arrays and pointer are two different things(we can check by applying sizeof). The confusion happens because array name indicates the address of first element and arrays are always passed as pointers (even if we use square bracket)

```c
// 1st program to show that array and pointers are different 
#include <stdio.h> 

int main() 
{ 
int arr[] = {10, 20, 30, 40, 50, 60}; 
int *ptr = arr; 
	
// sizof(int) * (number of element in arr[]) is printed 
printf("Size of arr[] %ld\n", sizeof(arr)); 

// sizeof a pointer is printed which is same for all type 
// of pointers (char *, void *, etc) 
printf("Size of ptr %ld", sizeof(ptr)); 
return 0; 
} 
```

OUTPUT
```
Size of arr[] 24
Size of ptr 8
```
- Assigning any address to an array variable is not allowed. 

**Arrays and Pointers look kindoff similar bacause:** 

-Array name gives address of first element of array.

- Array members are accessed using pointer arithmetic.
Compiler uses pointer arithmetic to access array element. For example, an expression like “arr[i]” is treated as * (arr + i) by the compiler. That is why the expressions like * (arr + i) work for array arr, and expressions like ptr[i] also work for pointer ptr.

- Array parameters are always passed as pointers, even when we use square brackets.

  
  ### What is vector in C++?
    
   Answer: Vector in C++ is a class in STL that represents an array. 
    
   **The advantages of vector over normal arrays are:**
        
- We do not need pass size as an extra parameter when we declare a vector i.e, Vectors support dynamic sizes (we do not have to initially specify size of a vector). 
- We can also resize a vector.
- Vectors have many in-built function like, removing an element, etc.
    

## JAVA
