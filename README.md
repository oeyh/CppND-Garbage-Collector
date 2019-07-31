# Garbage Collector Project from Udacity C++
The project implements my own version of a smart pointer, or more specificly a shared pointer. This is like implementing a garbage collector. I completed the following implementations and verified that it does not have any memory leaks with the leak tester.

## Codes implemented
- Completed `Pointer` constructor, destructor and operator== overloading
- Completed `PtrDetails` class

## Project structures
There are 3 classes defined in this project: `Pointer`, `PtrDetails` and `Iter`.
- `Pointer`. This is the class that defines a shared pointer similar to what C++ has. It can be used like a shared_ptr, with a generic data type and with three operators overloaded `*`, `->` and `[]`. `Pointer` also holds a static reference container of all memory blocks that have been allocated and the pointers point to it.
- `PtrDetails`. This class holds the reference count and address of a memory block. It is the elements in the static reference container in `Point` class.
- `Iter`. This class allows us to the use pointer arithmetic on `Pointer` object.
