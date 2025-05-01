# Allocators

## Requirements and Goals

### Handling arbitrary request sequences
An application can make an arbitrary sequence of allocate and free requests. The allocator cannot make any assumptions about the ordering of allocate and free requests. 

### Making immediate responses to requests
The allocator must respond immediately to allocte requests. The allocator can't re-order or buffer those requests

### Only use the Heap
In order to scale an allocator, any nonscalar data structures (linked lists, trees, arrays of structs, freelists, metadata structs for blocks) used by the allocator must be stored in the heap

### Aligning Blocks
The allocator must align blocks in such a way that they can hold any type of data object. This is relevant to how memory is padded to allow for the proper sizing of data

