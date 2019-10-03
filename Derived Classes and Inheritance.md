#### Derived Classes and Inheritance

#####C++ classes

- public and private keywords may be used
- member data and functions are in the corresponding classes

To pass ADTs in C requires passing a pointer. In C++, a <font color=red>this</font> pointer variable is automatically passed by the compiler.

###### Constructors

A constructor is a member function that has the same name as the class. A constructor runs automatically when a new object is created.

###### Function overloading

it's same to the overload in Java.

###### public vs. private

- By default, every member of a class is private

- private member is visible only to other members of the class
- public member is visible to anyone who sees the class declaration
- Not expose your variables by public
- Use get and set methods for your private variables

##### Derived classes and inheritance

(Actually, it's just like java, but code forms would be a bit different)

###### An Isosceles is a Triangle.

```c++
class Isosceles : public Triangle{}
```

Remember, the memory would be allocated for each one.

Because member functions are *inherited*, we don't need to rewrite them.

<font color = red>Even though they are inheritance-related, private variables cannot derived directly. Remember to call Set() function</font>

Constructors are not inherited, but the main file will call the parent class constructor first and then call the son class.