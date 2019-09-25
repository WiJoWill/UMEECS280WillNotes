#### ABSTRACT DATA TYPES in C

##### Data Abstraction

- seperate what a type from how the type is implemented
- C-style code, use a struct to implement the ADT
- ADT lets us model complex phenomena
- ADT makes programs easier to maintain & modify

<font color = red> What </font> means the meaning/purpose of the ADT; <font color=red>How</font> means the implement process of the ADT

In head file(.h), declare the struct and write the prototype of the functions. It's just like interfaces of java.

In cpp file, implement the functions.

When utilize ADT functions, be careful that some methods may have `const` when calling the input variables.

Remember to use an init function, because some structs (such as Triangles) need verification when being inited. 

Triangles are important in computer graphics.

##### Testing C-Style ADTs1

- Unit Testing
  - One piece at a time (a function)
- System testing
  - Entire project
- Regression testing
  - Automatically run all unit and system tests after a code change



##### Streams and stringstreams

- A stream acts an abstraction over
  - A source from which we can read data as input
  - A sink to which we can write data as output
  - Support character-based I/O from the terminal, files, etc.
- such as cout, cin, file I/O



