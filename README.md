# arrays-and-lists

We basically only use lists for DSA, the main difference between arrays and lists is that arrays can only store one data type whereas lists can store multiple data types

They use 0-based indexing

Adding Elements O(n):

    append() = add a single element at the end of the list
    extend() = add more than one element at the end of the list
    insert() = add an element at a specified position
    
Removing Elements O(n):

    pop() = remove an element from a specified position and return it
    remove() = remove an element with a specified value without returning it
    
Joining Lists:

We can only join lists with the same data type, to join them we use the + operator

Slicing Lists:

We slice lists with the : operator

    a:b = where a is the start index of our sub-list and b is the end index (we don't include b)
    
Looking up an element by its index is O(1) and looking up an element by its value is O(n)
