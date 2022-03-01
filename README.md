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
    
  
Strings:

Also use 0-based indexing

Strings are immutable in Python (we can't change the content of a string once it is initialised)


Sorting:

Selection Sort works by finding the minimum and moving it to the left each time

    class Solution:
    def sortArray(self, nums: List[int]) -> List[int]:
        
        #we will start from the beginning of our array
        for i in range(len(nums)):
            
            #assume that the first number in the list is the minimum
            minimum = i
            
            #we then compare this minimum with the rest of the list
            for j in range(i + 1, len(nums)):
                
                #if we find a smaller number
                if nums[j] < nums[minimum]:
                    
                    #then we set this as our new minimum
                    minimum = j
            
            #checks to see if a new minimum has been found
            if minimum != i:
                
                #if yes then swap the places of these
                nums[minimum], nums[i] = nums[i], nums[minimum]
        
        #return array which has been sorted by selection sort
        return nums
        
Bubble Sort works by comparing each value next to each other, after each pass the next largest number will be left on the far right

    class Solution:
    def sortArray(self, nums: List[int]) -> List[int]:
    
        #we can use this to break out our loop when it is fully sorted
        completeSort = False

        #stopping condition
        while not completeSort:

            #if no changes are made then completeSort will stay as true and the loop will break out
            completeSort = True

            #we can't create a bubble for the last number so iterate through up to the second to last element
            for i in range(len(nums) - 1):

                #if the number to the left is bigger than the number on the right
                if nums[i] > nums[i + 1]:

                    #state that we have performed a change
                    completeSort = False

                    #swap the values in the bubble
                    nums[i], nums[i + 1] = nums[i + 1], nums[i]

        #return array which has been sorted by bubble sort
        return nums
        
