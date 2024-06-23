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


# Some Important Points :
+ For any variable for any language the memory is created inside the Stack.
+ Data from the heap cannot be accessed Directly it should be accessed indirectly.
+ Stack Array Cannot be Resized.
+ Heap Array Can be Resized.

  
## For creating memory and Deallocation in heap :
+ C --->
  + For Memoryallocaton  :  (int*)malloc( number * size of int ).
  + For DeAllocation     :  free( variable name ).
+ C++ ->
  + For Memoryallocation :  new int [ number ].
  + For DeAllocation     :  delete [] variable_name .
