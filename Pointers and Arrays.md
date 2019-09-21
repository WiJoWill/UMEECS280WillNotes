### Pointers and Arrays

#####Memory

& refers to the address/a reference type

```int x = 3``` is different from ```int &x ```

However, remember that 

```cpp
int x = 5;
int &r = x;
//r = 5; r and x points to the same address
```

r is the new name for x

#####Pointer

a type of object whose value is the address of an object

```int *pointer ```

###### Derefence operator

- Pronounced as "dereference" or "indirection"
- "follows" the pointer to its object

```cpp
int x = 7;
int *p = &x;
cout << *p; // 7
```

Derefence operator is not same as a pointer type

###### Something to do with pointers

- Pointers let us work with objects <font color =red>indirectly</font>
  - Use objects across different scopes
  - keep track of objects in dynamic memory
- Pointers work with <font color=red>arrays</font> of objects
- Pointers are useful in C=programming

###### Kinds of objects in C++

- Atomic/primitive: int, double, char, etc, pointer types
- Arrays(homogeneous)
- Compound(hetergeneous)

##### Arrays

- fixed size
- elements of all the same type
- have ordered elements
- contiguous chunk of memory
- support  constant time random access by index
- Basic mechanism at the machine level
- library functions (vector) are built on top of arrays

The value of an array variable is  <font color=red>the address of the first element</font>.

Array turning into pointers has a lot of consequences. You can't assign arrays to each other.

##### Type Sizes

1. A char is always one byte -- 1
2. A short is always at least as big as a char -- 2
3. A int is always at least as big as a short -- 4
4. A long is always at least as big as an int -- 8

##### Pointer Arithmetic

Operators: +, -, +=, -=, ++, --, <, <=, >, >=, ==, !=

<font color=red>Warning!</font>Pointer arithmetic only makes sense in arrays!