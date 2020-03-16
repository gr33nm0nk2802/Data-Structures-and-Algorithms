-----
> Author : Syed Modassir Ali
> Date : 15.03.2020
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
  
  
  ### Difference between pointers and arrays in C?
  
    Answer: 
  
  ### What is vector in C++?
    
    Answer:
  
