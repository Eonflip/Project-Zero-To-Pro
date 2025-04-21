# The Heap

The heap can be understood as a section in a computers memory that has a bunch of blocks, each block is a chunk of virtual memory that is either allocated or free. 

Here's a simple diagram to illustrate the concept: 

<img src="./images/Heap-and-Stack.png" alt="Heap Diagram" height="500"/>

To elaborate a bit here, the Unintialized Data section is utilized for global static variables such as

```c
int global_count;
static float buffer[1024]; //Uninitialized array
```

Whereas initialized data is utilized to hold initialized global static variables

```c
int global_cound = 42;
static char name[] = 'Ian'; //Initialized character array
```

Code or .text is where you would find the compiled program instructions. 

These .bss, .data, and .text sections will show up in the assembly code, but we'll not cover that in this writeup. 

## Explicit Vs. Implicit Allocators

The Heap is usually accessed through something like an explicit or implicit allocator.

These will handle allocating, freeing and reallocating memory.

**Explicit Allocators** - are memory allocators that you have to call yourself and in the C standard library these are functions like malloc and free, whereas in C++ you'll find them as new and delete.

**Implicit Allocators** - handle memory automatically they detect when a program is no longer using a memory block and they free that memory block. These implicit allocators are also known as Garbage Collectors. Higher level languages usually have some form of garbage collector . Languages like Java, Python, JavaScript, Go, Ruby and C# all have garbage collectors.

