# The C Programmming Language

C is a high-level programming language developed in the early 1970s by Dennis Ritchie at Bell Labs. It is a **procedural language**, which means that it follows a top-down approach and uses **procedures or functions** to break down a problem into smaller, manageable tasks. C is widely used for system programming, embedded systems, and low-level programming, such as operating system and driver development. It is also a popular language for learning programming concepts and techniques, due to its simple and straightforward syntax. C is the basis for many other programming languages, such as C++, C#, and Java.

## Data Type and Symbols

| Data Type | Symbol | Size in bytes | Definition |
| ------ | ------| ------ | ------ |
| int | i, d or %i, %d | 2 or 4 | Intergers are whole numbers that can have both zero, positive and negative values but no decimal values, also sometimes called signed integers. eg **0, -5, 10 .** 
| double | lf or %lf | 8 | holds real numbers. eg **34.564e2.** 
| char | c or %c | 1 | character type
| float | f or %f | 4 | holds real numbers. eg **25.342e2.**
| short int | hd or %hd | 2 | 
| unsigned int | u or %u | 2 or 4 | type modifiers, You can  alter the data storage of a data type by using them. **unsigned -** allows for storage of only positive numbers. An `unsigned` data type is variable can hold non-negative integer values.
| long int | ld, li or %ld, %li | 4 or 8 |
| long long int | lld, lli or %lld, %lli | 8 |
| unsigned long int | lu or %lu | 4 |
| unsigned long long int | llu or %llu | 8 |
| signed char | c or %c | 1 |
| unsigned char | c or %c | 1 |
| long double | LF or %LF | 10 or 16 |
| size_t | zu or %zu | "size_t" is used to represent the size of an object. unsigned type integral.

#### Explain Type Modifiers

> There are four type modifiers in C that are used to alter the **Data Storage** of a data type:
> > The *Long* and *short* keywords - Long increases the size of an integer data type and short reduces the size of an integer data type.
> > 
> > The *signed* and *unsigned* keywords - these indicate whether a variable can hold negative or non-negative values respectively.
> >
> The Long keyword cannot be used with char or float types.
> 
> The main difference between the `unsigned` type modifier and the `signed` type modifier is that - `unsigned` holds a larger range of positive values but cannot hold negative values.


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

> Recursion is when a function calls itself repeatedly untill a specific task is accomplished, thus a recursive function.
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

Variables that are declared outside of all the functions are known as ***External variable or Global variables***. They are accesible from anywhere in the program. suppose, a global variable is declared in *file1*, if you try to  use that same variable in onother *file2*, the compiler will complain. To solve this problem, keyword ***extern*** is used in *file2* to indicate that the variable is an external variable declared in another file.

The ***register*** keyword is used to declare register variables. Register variables were supposed to be faster than local variables.

the `register` keyword is used to suggest to the compiler that a variable should be stored in a register rather than in memory. Register storage is faster than memory storage because the CPU can access registers directly, without the need to access memory.

When you define a variable with the `register` keyword, the compiler is free to ignore your suggestion and to store the variable in memory, depending on the available registers and the optimization level set.

It is important to note that not all types of variables can be defined as register variables. Variables that are defined as arrays or variables that have their address taken cannot be defined as register variables. Also, register variables have a limited scope, they cannot be used in function calls and cannot be passed to other functions.

In general, register variables are most useful in tight loops, where a variable is used repeatedly and its value changes frequently. For example, a variable that is used as a loop counter would be a good candidate for a register variable. 

Example :
```
> register int  i;
> 
>  for(i = 0; i < 1000; i++) 
>  
>  {
>  
>   do this
>   
>  }
```


The use of `register` keyword is mostly used as a hint to the compiler to store the variable in a register, but the actual storage location is up to the compiler to decide.

It is also worth noting that modern compilers are very good at optimizing code, and the use of the `register` keyword is less important than it used to be.

The ***Static*** variable is declared by using the static keyword, The value of the static variable persists until the end of the program. Eg. `static int i;`

### Arrays 

An Array is a collection of fixed number of values, once the size of an array is declared you cannot change it.

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

### Pointers 

Pointers are special variables that are used to store addresses rather than values. `int *a;`, `int* a, b`

Array names usually decay to pointers (meaning array names can sometimes be converted to pointers), you can use this pointer to access elements in an array. But you have to be careful not to change anything in the elements because it will change the elements in the original array.

> You can pass pointers as arguments in a function. 

### Memory Allocation in C

As you know, an array is a collection of a fixed number of values. Once declared, you cannot change it.

Sometimes the size of the array you declared may be insufficient. To solve this issue, you can allocate memory during run-time. This is known as dynamic memory allocation in C programming.

To allocate memory dynamically, library functions are `malloc()`, `calloc()`, `realloc()`, and `free()` are used. These functions are defined in the `stdlib.h` header file.

**`malloc()`** stands for *memory allocation*
The malloc() function reserves a block of memory of the specified number of bytes. And it returns a pointer of `void` which can be casted into pointers of any form. Syntax -> ptr = (castType*) malloc(size); Eg. ` *ptr = (float*) malloc(100 * sizeof(float));`

**`calloc()`** stands for *contiguous allocation* -> dataType *ptr = (castType*) calloc(n, size); 

**`realloc()`** stands for *reallocation of memory* -> The *`realloc()`* function in C is used to dynamically change the size of a previously allocated memory block. It takes a pointer to a previously allocated memory block and a new size as arguments, and returns a pointer to the newly allocated memory block. If the function is successful, the original memory block is freed and the returned pointer points to the newly allocated memory block. Eg: **`int *ptr = (int*) realloc(ptr 5 * sizeof(int))`**

**`free()`** Dynamically allocated memory  created with either `calloc()` or `malloc()` doesn't get freed on their own. we have to explicitly use `free()` to release the space.

### Strings

A string is a sequence of characters stored in an array with a null `\0` character marking the end of the string. Eg `char greet[] = {'h', 'e', 'l', 'l', 'o','\0'};` 

> Some few function to work with `string` keyword.
> 
> >  `strcat()` - to concatenate(joins) strings.
> >  
> >  `strcpy()` - Copies strings together.
> >  
> >  `strlen()` - computes strings length.
> >  
> >  `strcmp()` - compares two strings.
> >  
> >  `strlwr()` - converts (turns) strings to lowercase.
> >  
> >  `strupr()` - converts (turns) strings to uppercase.
> 

### Structures and Unions

 A **structure** is a user-defined data type that allows you to *group together* variables of different types into a single unit. A structure is defined using the keyword `struct`, followed by the name of the structure and a list of member variables inside curly braces. 
 
 when a struct type is created no memory or storage is allocated, To allocate memory or storage of a given structure type and work with it,  we need to create variables.
  
 ```
 struct StructureName {
 dataType memeber1;
 dataType member2;
 }
 ```
 
 Create a **Derived data type** *struct Person*
 
 ```
 struct Person {
 char name[50];
 int CitNo;
 float salary;
 }
 ```
 
 Accessing Members of a structure
 
 - (Dot) **.** member operator Eg. `person.salary`
 - (arrow) **->** Structure pointer operator (To access pointer members in struct)

We use **typedef** to create alias in structures 

```
typedef struct Distance {
    int feet;
    float inch;
} distances;

int main() {
    distances d1, d2;
}
```
 
 ### Unions 
 
 Both `Structures` and `Unions` are user-define data types that allow you to group together variables of different data types into a single Unit.
 
 > How ever there are few key differences between the two.
 
 1. Memory allocation: In a structure, *each member variable is allocated its own memory space*, whereas in a union, *all member variables share the same memory space*. This means that the total memory required for a union is equal to the memory required for the largest member variable, whereas the total memory required for a structure is equal to the sum of the memory required for all member variables.
 
 2. Accessing members: You can access the members of a structure using the dot operator (.) and you can access the members of a union using the dot operator or the arrow operator (->).
 
 3. Use cases: Structures are typically used when you need to group together related data items that have different types and that you want to be able to access independently. Unions, on the other hand, are typically used when you need to use the same memory space for variables that have different types, but you will only use one of them at a time.

It's important to note that unions can be useful in certain situations such as using the same memory space for different data types, but structures are more commonly used in C programming.

In general, structures are more versatile and can be used in a broader range of situations, whereas unions have more specific use cases and are generally used for optimization purposes.


















                                                                      
