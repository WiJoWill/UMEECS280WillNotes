####Container ADTs and Generic Programming

##### Containers

The purpose of container is to hold other objects, such as an array.

###### Set abstraction

1. insert a value into the set
2. remove a value from the set
3. determine if a value is a member of the set
4. count the number of elements in the set

###### static is confusing

- static function: visible only inside one file (internal linkage)
- static member variable: all instances of the Set class share this member variable

```const``` behind the method input value (out parentheses) means that they cannot change the private variable/values in the class.

private functions should not be exposed to the public. It can only be used in the class. 

Example/Practice

```c++
int Find (int v) const{
	for(int i = 0; i < numberOfElements; ++i){
		if(v == elements[i])
		{
		return i;
		}
	}
	return NumberAllocated;
}
```

Initialization Exercise

```c++
Set::Set():numberofElements(0){}
```



##### Generic Programming

1. Write the algorithm, specify the type later
2. C++ implements generic programming using the template mechanism

###### Template Notation

T is the type contained by this *Set*. It's like a variable name, and some programmers like to use *value_type* instead of T.

```c++
template <typename T>
	class Set
	{
	 public:
	 	void Insert(T v);//not use specified type
	}
```

