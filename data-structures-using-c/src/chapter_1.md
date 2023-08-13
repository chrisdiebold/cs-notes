# Introduction

Data Structure - a group of data elements that are put ptogether under one name, and which defines a particular way of storing and organizing in a computer so it can be used efficiently.

When selecting a data structure, folow these steps:
1. Analysis of the problem to determine basic operations; such as CRUD
2. Quantify the resource constraints for each operation
3. Select the data structure that best meets the requirements

There are 2 main classes of data structures: primititive and non-primitive
1. Primitive - the fundamental data types supported by the programming language
2. Non-Primititve - data types created from primitive data types

Non-Primitive data structures can be further classified in 2 categories: Linear and non-linear

Arrays, Linked Lists, Stacks and Queues are linear and Trees and Graphs are non-linear.

## Designing an Algorithm

There are 2 main approaches to design an algorithm: Top-down and Bottom-up.

Top Down approach - starts by dividing the complex algorithm into more or more modules. These modules can be further decomposed into one or more sub-modules, and this process of decomposition is iterated until the desired level of module compleity is acheived. 

Bottom-up approach - start by designing the most basic or concrete modules and then proceed towards designing higher level modules. The higher level modules are implemented by using the operations performed by lower level modules. Thus, in this approach sub-modules are grouped together to form a higher level module. All the higher level modules are clubbed together to form even higher level modules. This process is repeated until the design of the complete algorithm is obtained.

## Time and Space Complexity
Analysing an algorithm means determining the amount of resources (such as time and memory)
needed to execute it. 

Algorithms are generally designed to work with an arbitrary number of inputs, so the efficiency or complexity of an algorithm is stated in terms of time and space complexity.

The time complexity of an algorithm is basically the running time of a program as a function of the input size. 

Space complexity of an algorithm is the amount of computer memory that is required during the program execution as a function of the input size.


**Worst-case** running time This denotes the behaviour of an algorithm with respect to the worst-possible case of the input instance. The worst-case running time of an algorithm is an upper bound on the running time for any input. 

Therefore, having the knowledge of worst-case running time gives us an assurance that the algorithm will never go beyond this time limit.

**Average-case** running time of an algorithm is an estimate of the running time for an ‘average’ input. It specifies the expected behaviour of the algorithm when the input is randomly drawn from a given distribution. 

Average-case running time assumes that all inputs of a given size are equally likely.

**Best-case** running time is used to analyse an algorithm under optimal conditions. For example, the best case for a simple linear search on an array occurs when the desired element is the first in the list. However, while developing and choosing an algorithm to solve a problem, we hardly base our decision on the best-case performance. 

It is always recommended to improve the average performance and the worst-case performance of an algorithm.

**Amortized running time** refers to the time required to perform a sequence of (related) operations averaged over all the operations performed. Amortized analysis guarantees the average performance of each operation in the worst case.



