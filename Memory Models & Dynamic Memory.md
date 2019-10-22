#### Memory Models & Dynamic Memory

##### Logic Short-circuiting

##### Global & Local Variables

With global and local variables, you need to know two things at compile time(static)

1. The size ornumber
2. The lifetime(when created & destroyed)

- Global(Static) - lives for the whole program

- Local(Automatic) - lives during the execution of its local blcok

- Dynamic - you control the life time

###### Global

1. oustide of a function/class definition
2. as **static** within a function, or
3. as **static** within a class definition

<font color = red>static is not same to const</font>

###### Local

Only lives inside a {}block

- initialized when the declaration is run
- dies when the block is finished

###### dynamic variable

1. Its size is determined at runtime
2. when to create and destroy (or delete) it is determined at runtime

Create dynamic variables when using __new__

Pitfalls: dangling pointers, double delete, bad delete (but it's still okay to delete a nullptr, even if you cannot dereference a nullptr), memory leak 

```

```

