# Garbage Collector Project from Udacity C++
The project implements my own version of a smart pointer, or more specificly a shared pointer. This is like implementing a garbage collector. I completed the following implementations and verified that it does not have any memory leaks with the leak tester.

## Garbage collection algorithm
This project uses reference counting to perform garbage collection. 
"In reference counting, each dynamically allocated piece of memory has associated with it a reference count. This count is incremented each time a reference to the memory is added and decremented each time a reference to the memory is removed. In C++ terms, this means that each time a pointer is set to point to a piece of allocated memory, the reference count associated with that memory is incremented. When the pointer is set to point elsewhere, the reference count is decremented. When the reference count drops to zero, the memory is unused and can be released." -- From "The Art of C++" by Herbert Schildt.

## Project structure
There are 3 classes defined in this project: `Pointer`, `PtrDetails` and `Iter`.
- `Pointer`. This is the class that defines a shared pointer similar to what C++ has. It can be used like a shared_ptr, with a generic data type and with three operators overloaded `*`, `->` and `[]`. `Pointer` also holds a static reference container of all memory blocks that have been allocated and the pointers point to it.
- `PtrDetails`. This class holds the reference count and address of a memory block. It is the elements in the static reference container in `Point` class.
- `Iter`. This class allows us to the use pointer arithmetic on `Pointer` object.

## Codes implemented
- Completed `Pointer` constructor, destructor and operator== overloading
- Completed `PtrDetails` class
