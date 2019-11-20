#### Recursion & Tail Recursion

##### Recursion

Functions can call other functions. In recursion, it calls itself.

```c++
int factorial (int n)
{
if(n == 0) return 1;
return n * factorial(n - 1);
}
```

##### Tail Calls

a function call is a <font color = red>tail call </font> if it's the very last thing in its containing function.

The calling function has no pending work to do after a tail call (in the passive call). 

###### Tail call optimization

- most compilers are able to recognize tail calls and optimize them, reusing the current stack frame for new recursive call
- With g++, the -O2 and -O3 options include tail call optimization
- Tail call optimization can take a recursive algorithm from linear to \\

We define a function as <font color=red>tail recursive</font> if ALL the recursive calls it makes are tail calls.



- Not tail recursive

- ```c++
  int log2(int x)
  {
  	if(x == 1) return 0;
  	return 1 + log2(x/2);
  }
  ```

- Tail recursive

- ```c++
  void countdown1(int n)
  {
  	if(n <= 0) return;
  	cout << n << endl;
  	countdown1(n - 1);
  	return;
  }
  ```

