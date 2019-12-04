#### Containers of Pointers

Containers use template, so they can hold any type.

#####Containers of pointers: motivation

1. Avoid slow copies of big objects.
2. Allows you to manage the lifetime of the variable yourself.
3. Allows you to create unique objects shared on multiple lists.
4. Useful when many parts of the code refer to an object, but
you only want one copy in memory.
5. <font color=red>Also useful for polymorphism</font>



When using containers of pointers, we should care for dynamic memory. **node->datum** may have some dynamic objects in heap, so we always use a for loop to delete.

```c++
for(auto i: list){
	delete i;
}
```

#####Containers-of-pointers are subject to two broad kinds of bugs.

1. Dangling pointers: Using an object after it has been deleted.
2. Memory leaks: Leaving an object orphaned by never deleting it.

