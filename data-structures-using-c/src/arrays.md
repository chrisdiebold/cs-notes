# Arrays

An array is a collection of similar data elements. These data elements have the same data type. 

The elements of an array are stored in consecutive memory locations and are referenced by an index. 

## Declaring an Array
There are 3 components to array declaration:
1. Data Type - the kind of values to store: int, char, float, double, etc.
2. Name - to identify the array
3. Size - the maximum number of values that the array can hold

```c
// type name[size]
int marks[10];
// array indices 0-9
```
An array index starts at 0. 

## Accessing elements of an array
To access all the elements, we must use a loop. That is, we can access all the elements of an array by varying the value of the subscript into the array. But note that the subscript must be an integral value or an expression that evaluates to an integral value. 

```c
// set each element of the array to -1
int i, marks[10];
for(i = 0; i < 10; i++)
    marks[i] = -1;
```
### How C gets to know where an individual element of an array is located in the memory?

 The answer is that the array name is a symbolic reference to the address of the first byte of the array. 
 
 When we use the array name, we are actually referring to the first byte of the array.

The subscript or the index represents the offset from the beginning of the array to the element being referenced. That is, with just the array name and the index, C can calculate the address of any element in the array.

```
Address of data element, A[k] = BA(A) + w(k – lower_bound)

 A is the array, k is the index of the element of which we have to calculate the address, BA is the base address of the array A, and w is the size of one element in memory, for example, size of int is 2.
```

### Length of an array
The length of an array is given by the number of elements stored in it. The general formula to calculate the length of an array is

```
Length = upper_bound – lower_bound + 1
```
