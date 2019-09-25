



#### Compound Objects

##### stream input, cin, and fstream

stoi() -- parses an integer value encoded in a C++ string

```c++
cout << "Enter numbers to sum:" << endl;
string input_value;
int sum = 0;
while(cin >> input_value && input_value != "done"){
	sum += stoi(input_value);
}
cout << "sum is " << sum << endl;
```

fstream: read and write files directly with the fstream library

Common Mistakes

1. The check falls behind

```c++
while(!fin.fail()){
	fin >> word;
	cout << word;
}
```

2. 

```
while(!fin.eof()){
	fin >> word;
	cout << word;
}
```

Input & Output;

```c++
Input: ifstream fin;
Output: Ofstream fout;
```



##### Compound types

A <font color = red>compound type</font> is datatype that we define in our code as containing other primitive or compound data types.

1. Primitives
2. Arrays
3. <font color=red>Compound</font>(heterogeneous: special characteristics of the compound)



##### Struct

1. struct is the simplest compound type in C and C++
2. elements in a struct are laid out in memory in the <font color=red>order listed </font>

If a struct has 4 elements but, when being defined, only three elements are defined, the last one will be undefined.

```c++
Struct a = xxxx;
Struct b = a;
//All of the members are copied
```



##### Passing structs to functions

By default, structs are passed by value, copying the entire struct onto the stack. In order to decrease space used, programmers always use pointer or reference (let compiler create pointers).

Use the const keyword to prevent from being changed.



##### Arrays of structs

Composable data types: Once you have declared a type struct x, that type can be used to define a pointer to struct x, an array of struct x, or even a struct that contains a struct x.

If we define a struct as Triangle, we can do 

```c++
const int Size = 3;
Triangle triangles[Size];
triangles[0] = {3, 4, 5};
triangles[1] = {5, 12, 13};
triangles[2] = {8, 15, 17};
```



##### structs vs arrays



```c++
struct students{
  int num;
  int stu_id[num];
  int group_id;
}
```

