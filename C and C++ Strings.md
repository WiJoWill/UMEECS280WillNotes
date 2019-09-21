#### C and C++ Strings

###### C-style strings

Equivalent:

- ``` char s[5] = {'c', 'o', 'd', 'e','\0'};```
- ```char s[] = "code";```

If mismatch the size and real initialized value, the compiler automatically puts '\0' at the end of string literals.



Pointer EXERCISE: 

//REQUIRES: "a" points to an array of length "size"
//EFFECTS: Returns a pointer to the first
// occurrence of "search" in "a".
// Returns NULL if not found.

int *find( int *a, int size, int search );

//REQUIRES: "s" is a NULL-terminated C-string
//EFFECTS: Returns a pointer to the first
// occurrence of "search" in "s".
// Returns NULL if not found.

```cpp
int *find(int *a, int size, int search){
    for(int *ptr = a; ptr < a + size; ++a){
        if(*ptr == search)
            return ptr;
    }
    return NULL;
}

char *strchr(char *s, char search){
    while(*s){
        if(*ptr == search)
            return ptr;
      ++s;
    }
    return NULL;
}

```



