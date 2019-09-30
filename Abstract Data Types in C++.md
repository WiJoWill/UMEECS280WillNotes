

#### Abstract Data Types in C++

#### On to classes

###### C++ styles

- contains data and functions
- constructors can be used to initialize
- control of data access

A class has both **member data** and **member functions **.

It seems that class gives more clear definition such as initializing  functions, but struct only defines the parameters in the struct.

Like Java and other languages, the parameter should be protected by private, but functions should be public to accessed.

<font color=red>Be careful of the default access</font>: class is private but struct is public

##### Constructors

There are three avaiable ways to use Constructor

```c++
Triangle t1;
Triangle t2(3, 4, 5);
Triangle t3 = Triangle(3,4,5);
```

But remember, this is declaration of function not calling constructor to create a new instance

```Triangle t4();```

Remember differences between assignment and initialization.

```c++
//assignment
Triangle(double a_in, double b_in, double c_in){
	a = a_in;	
  b = b_in;
  c = c_in;
}
```

```c++
//initialize
Triangle(double a_in, double b_in, double c_in):a(a_in), b(b_in), c(c_in){
		//nothing to do here
}
```

Initialization can be done both explicitly and implicitly(default).

###### Default initialization

- Atomic objects are default initialized by doing nothing

- Array objects are default initialized by default initializing each element
- Compound objects are default initialized buy calling the default constructor.
  - Default constructor does not has any parameters actually.

###### Check Invariants

Since we don't have access to private parameters directly, we use get and set

- Get: only return them
- Set: Remember to check whether the input value for setting the parameters are acceptable; 

