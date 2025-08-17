**
# Array Manipulation Algorithms

Array manipulation algorithms are essential for efficiently handling and processing data stored in arrays. This document provides an overview of common array manipulation techniques along with examples.

## Common Array Manipulation Techniques

### 1. Insertion
Inserting an element into an array involves shifting elements to make space for the new element.

**Example:**
```python
def insert_element(arr, index, element):
    arr.append(0)  # Increase the size of the array
    for i in range(len(arr) - 1, index, -1):
        arr[i] = arr[i - 1]  # Shift elements to the right
    arr[index] = element  # Insert the new element
    return arr
```

### 2. Deletion
Deleting an element from an array requires shifting elements to fill the gap left by the removed element.

**Example:**
```python
def delete_element(arr, index):
    for i in range(index, len(arr) - 1):
        arr[i] = arr[i + 1]  # Shift elements to the left
    arr.pop()  # Remove the last element
    return arr
```

### 3. Searching
Searching for an element in an array can be done using linear search or binary search (for sorted arrays).

**Example of Linear Search:**
```python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i  # Return the index of the target
    return -1  # Target not found
```

### 4. Sorting
Sorting an array can be achieved using various algorithms such as bubble sort, selection sort, or quicksort.

**Example of Bubble Sort:**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]  # Swap
    return arr
```

## Conclusion
Understanding these array manipulation techniques is crucial for solving complex problems efficiently. Practice implementing these algorithms to enhance your programming skills.
