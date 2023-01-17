# The C Programmming Language

C is one of the oldest programming languages *some consider it to be the mother of all programming languages*.
It is an **Imperative** **Procedural** typed language.

**Imperative** means it is has a clearly defined sequence of instructions in a program.
**Procedural** means it divides tasks a program is suppose to do into smaller sub-tasks.

## Data Type and Symbols

| Data Type | Symbol | Size in bytes | Definition |
| ------ | ------| ------ | ------ |
| int | i, d or %i, %d | 2 or 4 | Intergers are whole numbers that can have both zero, positive and negative values but no decimal values, also sometimes called signed integers. eg **0, -5, 10 .** 
| double | lf or %lf | 8 | holds real numbers. eg **34.564e2.** 
| char | c or %c | 1 | character type
| float | f or %f | 4 | holds real numbers. eg **25.342e2.**
| short int | hd or %hd | 2 | 
| unsigned int | u or %u | 2 or 4 | type modifiers, You can  alter the data storage of a data type by using them. **unsigned -** allows for storage of only positive numbers. 
| long int | ld, li or %ld, %li | 4 or 8 |
| long long int | lld, lli or %lld, %lli | 8 |
| unsigned long int | lu or %lu | 4 |
| unsigned long long int | llu or %llu | 8 |
| signed char | c or %c | 1 |
| unsigned char | c or %c | 1 |
| long double | LF or %LF | 10 or 16 |
| size_t | zu or %zu | "size_t" is used to represent the size of an object. unsigned type integral.

> The Long keyword cannot be used with char or float types.


### Derived Data Types
Data types that are derived from fundamental data types are derived types. Eg, **arrays, pointers, function types, structures, bool type, Enumerated type, Complex types.**

> In **if else** you do not need to put **{ }** if there is only one statement in it.

``` 
 if ( a%y == x) {
   do this
  } else if ( a == x ) {
   do this
  } else {
   do this
  }
```

### Loops

In C language we use loops to iterate or do something repeatedly.

* for Loops 
` for(int a = 0; a <= x; a++) {do this}`

* while Loops
`while ( a <= x ) {do this}`

* do while loops
`do {do this} while(a <= x)`

### Functions in C language - a function is a block of code to excute a specific task.
There are two type of functions in C 
* user-defined functions - created by a user.
* standard library functions - functions in the header files of c language.

> Recursion is when a function calls itself untill a specific task is accomplished, thus a recursive function.
>> sometimes it is best to use loops instead of recursions as they are slower.
>> but recursive functions have their use cases in Data structures and Algorithm.

### Storage Classes

Every variable in C has both a Type and a Storage class.
> **Type** - Means the data type of a variable.
> **Storage Class** - Determines the scope, visibility and lifetime of a variable.

#### There are Four type of Storage Class

- static
- register
- external
- automatic

*automatic or local variables* - this are variables that are local to the block in which they are declared. Eg. A variable declared inside a for loop or a function, that variable is local to that block of code.

Variables that are declared outside of all the functions are known as ***External variable or Global variables***. They are accesible from anywhere in the program. suppose, a global variable is declared in *file1*, if you try to  use that same variable in onother file *file2*, the compiler will complain. To solve this problem, keyword ***extern*** is used in *file2* to indicate that the external variable is declared in another file.

The ***register*** keyword is used to declare register variables. Register variables were supposed to be faster than local variables.

The ***Static*** variable is declared by using the static keyword, The value of the static variable persists until the end of the program. Eg. `static int i;`

### Arrays 

> An Array is variable that can store multiple values Eg. `float marks[3] = { 65, 45, 56 };`

Declaring an Array - dataType arrayName [arraySize] = { arrayElements }

> An array can be one Dimensional or multi-Dimensional array.
>
>> One Dimensional Array -> int marks[5] = {2, 3, 4, 5, 1}
>
>> Multi Dimensional Array (2D array) -> int marks[5][5] = {{1, 3, 4, 5, 6},{2, 2, 34, 5, 6}}
> 
>> Multi Dimensional Array (3D array) -> int marks[5][5][5] = { {1, 3, 4, 5, 6}, {2, 2, 34, 5, 6}, {2, 3, 4, 5, 1} }
> We use for Loops to iterate over values of multi-Dimensional arrays.
> When passing a 2 dimensional array in a function as a parameter it is not mandatory to specify the number of rows in an array, how ever its mandatory to specify the number of columns.














                                                                      
