# arrays-and-lists

We basically only use lists for DSA, the main difference between arrays and lists is that arrays can only store one data type whereas lists can store multiple data types

Accessing Elements:

Lists in Python use 0-based indexing

    list[index] = access element in a 1D list 
    list[index][sub-index] = access element in a 2D/nested list

They use 0-based indexing

Adding Elements O(n):

    append() = add a single element at the end of the list
    extend() = add more than one element at the end of the list
    insert(index, val) = add an element at a specified position
    
Removing Elements O(n):

    pop() = remove an element from a specified position and return it
    remove() = remove an element with a specified value without returning it
    
Joining Lists:

We can only join lists with the same data type, to join them we use the + operator

Slicing Lists:

We slice lists with the : operator

    a:b = where a is the start index of our sub-list and b is the end index (we don't include b)
    
Searching for Elements in a List:

We have two methods for searching: linear search and binary search

    Linear Search is where check each element one by one until we find the target value, the time complexity is O(n)

    Binary Search only works if our list is sorted, we repeatedly find the midpoint and determine whether our target value is to the left or right

Binary Search is much faster than Linear Search but if our list is not sorted then it is faster to do Linear Search as it would take longer to sort the list and then perform a Binary Search
    
Looking up an element by its index is O(1) and looking up an element by its value is O(n)

Iterating Through Lists:

    for = used when the number of iterations are known
    
    for i in list = i has the value of each element
    
    for i in range(len(list)) = i has the index of each element
    
    while = used when the number of iterations is unknown

2D Lists:

    To return number of rows we use len(list)
    
    To return number of columns we use len(list[0])

Unique Tools:

    index(element) = returns the index of the specified element in the list
    
    reverse() = reverses the list
