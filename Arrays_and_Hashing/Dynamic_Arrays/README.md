# Dynamic Arrays

Dynamic arrays are an extension of static arrays, offering more flexibility. Unlike a static array, which has a fixed size, a dynamic array can grow or shrink in size as needed.

## Key Concepts:

1. Static vs. Dynamic Arrays:
   - Static Array: A fixed size array where the number of elements is determined at the time of creation. Once set, the size cannot be changed.
   - Dynamic Array: A resizable array that allows elements to be added or removed, automatically resizing as needed.

2. Resizing:
   - When a dynamic array reaches its capacity (i.e., the number of elements equals the current size of the array), it needs to resize to accommodate new elements.
   - Typically, the array is resized by allocating a new array with a larger capacity, copying the elements from the old array to the new one, and then releasing the old array.
   - The resizing factor is often 2, meaning the array size doubles when resizing occurs.

3. Amortized Time Complexity:
   - While adding a single element might seem costly when resizing is needed, the average time per insertion over a series of insertions is low.
   - This is because resizing doesn’t happen every time an element is added. The time complexity for inserting an element into a dynamic array is O(1) on average (amortized time).

4. Memory Considerations:
   - Dynamic arrays require more memory than static arrays because they need to manage the extra capacity. However, this extra space ensures that the array can grow efficiently.

5. Advantages:
   - Flexibility: You don't need to know the number of elements in advance.
   - Efficient: On average, insertions are fast due to the amortized time complexity.

6. Disadvantages:
   - Overhead: Extra memory is required to handle resizing.
   - Copying: Resizing involves copying elements, which can be costly in terms of time and memory.

### Example in Python:

Python’s `list` is an example of a dynamic array. Here’s how it works:

```python
# Initializing a list (dynamic array)
arr = []

# Adding elements (the list automatically resizes as needed)
arr.append(1)
arr.append(2)
arr.append(3)

print(arr)  # Output: [1, 2, 3]

# Accessing elements
print(arr[0])  # Output: 1

# Removing elements
arr.pop()  # Removes the last element
print(arr)  # Output: [1, 2]
```

Here’s what happens under the hood:

- When you append an element and the list is at capacity, Python creates a new list with more space, copies the elements from the old list, and then appends the new element.
