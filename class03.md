# class03 Reading Notes:

## Java Primitives versus Objects:
![Primitives versus Objects](https://i.pinimg.com/originals/4a/64/db/4a64db4f5c8176b9c6da41f22729596d.jpg)

* wo-fold type system consisting :
1. Primitives(int,float)
2. Reference(Int,Float)

* autoboxing: 
The process of converting a primitive type to a reference one

### the primitive type variables have the following impact on the memory:
- boolean – 1 bit
- byte – 8 bits
- short, char – 16 bits
- int, float – 32 bits
- long, double – 64 bits

### the Reference type variables have the following impact on the memory:
- Boolean – 128 bits
- Byte – 128 bits
- Short, Character – 128 bits
- Integer, Float – 128 bits
- Long, Double – 192 bits

### The performance of a Java code depends on :

1. The performance of a Java code
2. on the compiler
3. on the state of the virtual machine
4. on the activity of other processes in the operating system.

![Primitives vs Reference](https://www.scientecheasy.com/wp-content/uploads/2018/06/memory-allocation.png)

###  Default Values:
* Default values of the primitive types are 0 ,false for the boolean type,\u0000 for the char type
* Default for reference types might acquire a value (null) that in some sense doesn't belong to their domains.

### Usage: 
* he primitive types are much faster and require much less memory

* objects in Java are slower and have a bigger memory.



## Exceptions:
![Exceptions](https://media.geeksforgeeks.org/wp-content/uploads/Exception-in-java1.png)
* An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

* exception object, contains information about the error, including its type and the state of the program when the error occurred.

* call stack:The set of possible "somethings" to handle the exception is the ordered list of methods that had been called to get to the method where the error occurred

* exception handler:The runtime system searches the call stack for a method that contains a block of code that can handle the exception

## Scanning:
*  scanner uses white space to separate tokens. (White space characters include blanks, tabs, and line terminators