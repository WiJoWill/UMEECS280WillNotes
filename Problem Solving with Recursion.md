#### Problem Solving with Recursion

##### Tree Print

```c++
void PrintTreeInOrder(Node *n){
	if(n){
		PrintTree(n->left);
		cout << n->datum << " ";
		PrintTree(n->right);
	}
}
```

