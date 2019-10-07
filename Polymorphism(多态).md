####Polymorphism(多态)

##### Derived Classes

This creates a new type called Isosceles that contains <font color=red>*all of the Triangle member functions and member data* </font>.

```c++
class Isosceles : public Triangle{}
```

Default constructor initialize the variables with 0.

###### Order of Execution

- Base class constructors run even without a constructor for the derived class.
- Constructors run in the order the members appear in the class.

Base class constructors always run.

###### Order of execution

- If a class inherits both Base2 and Base 3 in the order of ```: public Base2, Base3```, the order of execution will be that Base2 goes first, and Base3 goes next, even though the function call ```: Base3(). Base2()```

######Benefits of derived classes

- **Implementation inheritance**: Save implementation effort by sharing functions provided by the base class.

- **Interface inheritance**: Allow different derived classes to be used interchangeably through the interface provided by a common base class.

##### Polymorphism

Definition: A single interface to objects of different type. For example, You ask for an Animal object to makes its sound and it make the appropriate sound whatever type of animal it is. 

###### Liskov Substitution Principles

- If S is a subtype of T, then objects of type T may be replaced with objects of S.
- Functions that use pointers to base classes can use objects of derived classes without knowing it.

Dynamic Types: Remember to *delete* after creatinga dynamic object. <font color=red>virtual</font> means "check the dynamic type at runtime, then select the correct print( ) member function". virtual is also inherited. 

Polymorphism is the ability to associate many behaviors with one function name.

Pure virtual functions:

- Declare each method as a virtual function

- "Assign" a 0 to each of these virtual functions

- ```c++
  class Shape
  {
  	public:
  		virtual double area() const = 0;
  		virtual void print() const = 0;
  }
  ```

- Shape is now an abstract class, or *interface only* class.
- <font color=red>You cannot create an instance of an abstract class, but you can create a pointer to an abstract class and then assign the pointer to a concrete class derived from the base class.</font>

Upcast & Downcast: Upcast conversion is automatic, but Downcast is not. Higher hiearchy classes may not have all functions and variables in lower hierarchy classes.