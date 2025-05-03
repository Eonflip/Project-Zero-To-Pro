# Allocators

## Requirements and Goals

### Handling arbitrary request sequences
An application can make an arbitrary sequence of allocate and free requests. The allocator cannot make any assumptions about the ordering of allocate and free requests. 

### Making immediate responses to requests
The allocator must respond immediately to allocte requests. The allocator can't re-order or buffer those requests

### Only use the Heap
In order to scale an allocator, any nonscalar data structures (linked lists, trees, arrays of structs, freelists, metadata structs for blocks) used by the allocator must be stored in the heap

### Aligning Blocks
The allocator must align blocks in such a way that they can hold any type of data object. This is relevant to how memory is padded to blocks of 8 bytes allow for the proper sizing of data

### Not Modifying Allocated Blocks
Allocators can only manipulate or change free blocks. They are not allowed to move or modify blocks once they are allocted. 

## Goal 1: Maximizing Throughput

Given some sequence of n allocate and free requests we would like to maximize an allocator's throughput, which is defined as the number of requests that it completes per unit time. 

## Goal 2: Maximizing Memory Utilization. 

Virtual memory is NOT unlimited, in fact virtual memory is bounded by the amount of swap space on a disk. 



## Allocator Implementation Considerations

### Free Block Organization
How do we keep track of free blocks? 

### Placement
How do we choose an appropriate free block in which to place a newly allocated block?

### Splitting
After we place a newly allocated block in some free block, what do we do with the remainder of the free block

### Coalescing
What do we do with a block that has just been freed? 


# Implicit Free Lists
This is a test
