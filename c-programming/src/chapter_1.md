# Introduction

C is a low level programming language. C exposes machine level concpets that other languages try to hide, i.e. bytes and addresses. C also provides operations that correspond closely to a computers built in instructions, so that programs can be fast. 

C is a small language. C provides a more limited set of features than many languages. To keep the number of features small, C relies heavily on a library of standard functions. 

C is a permissive language. C assummes that you know what you are doing, so it allows you a wider degree of latitude than many languages. C doesn't mandate the detailed error-checking found in other languages. 

## Strengths
- Efficiency. Because C was intended for application where assembly language had traditionally been used, it was crucial that C programs could run quickly and in limited amounts of memory. 
- Portability. When a program must run on computers ranging from PCs to supercomputers, it is often written in C. One reason for the portability is that it is standardized through ANSI/ISO standards when prevents the language from splintering into incompatible dialects. Another is that C compilers are small and easily written, which helped make them highly available. 
- Power. C's large collection of data types and operators help make it a powerful language. 
- Flexibility. C was designed for systems programming, but is not restricted to this field. C is now used for applications of all kinds from embedded systems to commercial data processing. 
- Standard Library. C ships with a library that contains hundreds of function for I/O, string handling, storage allocation, and other useful operations. 
- Integration with Unix.

## Weaknesses
Many of C's weaknesses arise from its closeness to the machine. 

- C programs can be error-prone. C's flexibility make it error-prone. Programming mistakes that would be caught in many other languages cannot be detected by a C compiler. In this respect, C is a lot like assembly language, where most errors are not detected until a program is run. To make matters worse, C contains a number of pitfalls for the unwary. 
- C programs can be difficult to understand. 
- C programs can be difficult to modify. Large prorams written in C can be hard to change if they have not been designed with maintenance in mind. C lacks code organization features such as modules and namespaces.  

# Compiling and Linking

After we have written some code we need to compile our program to run it. Compiling is more involved that you might expect. Here are the steps:
- Preprocessing. The program is given to a preprocessor, which obeys commands that begin with a `#`, known as a directive. 
- Compiling. The modified program now goes through a compiler, which translates it into machine instructions (object code). The program is not quite ready to run yet.
- Linking. In the final step, a linker combines the object code produced by the compiler with any additional code needed to yield a complete executable program. Additional code being any code included in your program through preprocessing. 

> cc -o <executable_name> <files.c>
> gcc -O -Wall -W -pedantic - ansi -std=c99 -o executable files.c


# Building Blocks

## Functions
Functions are like procedures or subroutines in other programming languages. In fact, a C program is little more than a collection of functions. Functions fall into 2 categories: functions written by the programmer or library functions

In C, a function is a series of statements that have been grouped together and given a name. Some functions compute a value; some do not. A function that computes a value uses a `return` statement. 


C requires statements to end with a semicolon. The semicolon shows te compiler where the statement ends. Directives do not end in a semicolon. 

## Comments

A comment is documenation. C has this kind of comment.

```C
/* C Style Comment */

// This kind of comment was added in C99. This type is safer.

```

## Constants

Constants are create by using a macro definitiion. 

```C
#define INCHES_PER_POUND 166

#define FLOAT_CONSTANT 123.09f
```

