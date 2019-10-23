Managing Dynamic Memory

##### Modify the container to use dynamic memory

Provide variables to change the size rather than restricted size.

````c++
class UnorderedSet
{
private:
int *elements; //pointer to dynamic array
int numberOfElements; //current occupancy
int NumberAllocated; //capacity of array
static const int DefaultNumberAllocated = 100;
}
````

_elements_ will point to a dynamic array, *NumberAllocated* tells us the size of the allocated array.

```c++
UnorderedSet::UnorderedSet( int capacity ) :
numberOfElements ( 0 ), NumberAllocated( capacity )
{
	elements = new int[ NumberAllocated ];
}
```

Recall that this is called function overloading: 2 different functions with the same name but different prototypes.

Destructor

```c++
~classname();
```

Destructors run automatically when an object is detroyed

- local variables: when it goes out of scope
- global variables: when the program ends;



1. Observation: the compiler is terrible at managing resources
   - If we use new to create dynamic memory, the compiler can’t clean it up for us

2. Observation: the compiler is good at managing local variables
  - Automatic storage duration
  - Cleaned up when they go out of scope

Solution: wrap up resource management in a class and use local instances of the class to access the resources

- That's what we did with ctors and dtors

For the dynamic array, we can use array to change the size of the array

```c++
void UnorderedSet::grow(){
	int *temp = new int [NumberAllocated++];
	for(int i = 0; i < numberOfElement ;++i){
		temp[i] = elements[i];
	}
	delete[] elements;
	elements = temp;
}
```

##### growing

Optimizing grow()

```c++
void UnorderedSet::grow( )
{
int *tmp = new int[ NumberAllocated * 2 ];
for ( int i = 0; i < numberOfElements; ++i )
tmp[ i ] = elements[ i ];

delete[ ] elements;
elements = tmp;
NumberAllocated *= 2;
}
```

##### Destructors

if the destructor of base class is not virtual function, when creating a pointer of base class to derived class, the correct distructor will not be called. In this way，**virtual it** in the base class.