#### Structural Recursion

recursive list size function

```c++
int ListSize(Node *n, int size){
	if(n == nullptr){
    return size;
  }
  size++;
  return ListSize(n->next, size);
}
```

You can put this into a helper method, which start with size = 0;

ListMax function

```c++
int ListMax(Node *n){
// Base case
if ( n->next == nullptr )
return n->datum;
// Recursive case
return max( n->datum, ListMax( n->next ) );
}
```

##### Recursion and Iteration Summary

1. Recursion requires a new stack frame for each call, which can be
expensive.
2. We can always rewrite a recursive solution into an iterative solution that uses a stack. (That's what the compiler is doing using the call stack.)
3. Sometimes, we can rewrite a recursive solution into an iterative
solution that doesn't need the stack.
4. That's called tail recursion and the compiler can do the rewriting for us.
5. Tail recursion and iteration are two ways of writing the same thing.
6. We've seen that we can find the maximum element in a list using
either iteration or tail recursion.
7. So this is really design decision, your chance to pick which solution
you like better.

##### Trees

###### TREE size

```c++
int TreeSize( Node *n )
{
// Base case
if ( n == nullptr )
return 0;
// Recursive case
int leftSize = TreeSize( n->left );
int rightSize = TreeSize( n->right );
return 1 + leftSize + rightSize;
}
```

###### TREE HIEGHT

```c++
int TreeHeight( Node *n )
{
if ( !n )
return 0;
return 1 + max( TreeHeight( n->left ),
TreeHeight( n->right ) );
}
```

