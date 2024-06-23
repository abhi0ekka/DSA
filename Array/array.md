# Array :
+ Collection of similar data elements are called as Array.
  
## Basic things on Array :
+ Declaration of an Array.
+ Assiging value to the Array.
+ Access value of the Array.

  
## Static vs Dynamic Array :

### Static Array :
+ Static Array is that in which size is declared at the Complie time.
+ For example in C-Programming language the size must be created at the compile time.

   
### Dynamic Array :
+ Dynamic Array is that in which size is declared at the Run Time.
+ But in C++ Programming language size of the Array can be created at the Run Time.


## 2-Dimensional Array
+ In 2-Dimensional Array we can store the value in 2Dimension in rows and column.

### Declaration of 2-Dimensonal Array:
1. Normally like the Linear-Dimenson Array.
2. Using the Pointer Array
   * In which all the Pointer Array Points different array in the Heap.
   * In this pointer array is in stack and pointing array is in the heap.
   * In this the pointer array and the variable is in the stack.
3. Using double Pointer Array
   * In this just one step above from the second point.
   * In this all the array is in the heap.
   * only the variable is created in the stack.
### Accessing 2-Dimensonal Array:
* We use Nested for loop to access the element of the array.




# How Compiler Access the element:
* when the array is created it is created in the stack with some base address.
  * when we try to access the element of the array.
    * It uses the formula : <span style="color: red;"> base address + element_access * size_of_data_type </span>.
      * If we have some other programming language which indexing start with 1 then we will just modify the formula element_access will be element_access-1. 




# How 2-Dimensonal Array are managed by the Compiler:
+ So, when we think of a 2Dimensonal array.
+ The first thing come to mind is that it will be stored in row and column.
+ But that not the case the 2Dimensonal array are stored linearly in the memory.

## Ways of mapping 2Dimensonal Array:
1. Row Major Mapping.
2. Column Major Mapping.

### Row Major Mapping :
The element are stored in linear way in the format row by row.

### Column Mojor Mapping :
The element are stored in linear way in the format of column by column.

## The Row Major Formula and Column Major are almost the same so there is no difference so compiler can use any of them.
# Some Important Points :
+ For any variable for any language the memory is created inside the Stack.
+ Data from the heap cannot be accessed Directly it should be accessed indirectly.
+ Stack Array Cannot be Resized.
+ Heap Array Can be Resized.
+ Compiler uses formula to access the address for the Array.

  
## For creating memory and Deallocation in heap :
+ C --->
  + For Memoryallocaton  :  (int*)malloc( number * size of int ).
  + For DeAllocation     :  free( variable name ).
+ C++ ->
  + For Memoryallocation :  new int [ number ].
  + For DeAllocation     :  delete [] variable_name .
