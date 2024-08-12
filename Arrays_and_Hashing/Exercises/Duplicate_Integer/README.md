# Duplicate Integer (Easy)

Given an integer array nums, return true if any value appears more than once in the array, otherwise return false.

## Example 1

```python
Input: nums = [1, 2, 3, 3]

Output: true
```

## Example 2

```javascript
Input: let nums = [1, 2, 3, 4]

Output: false
```

## Solution

### 1. Thought Process

- Consider Edge Cases
  - Empty array: If the array is empty, there can't be any duplicates, so you should return false.
  - Single-element array: If the array has only one element, it can't have duplicates, so you should return false.
- Strategies to use
  - Nested loop: Compare each element with every other element in the array. `Time complexity > O(n^2).` \
  Not very efficient.
  - Sorting an array: Sort an array into an order e.g. ascending to descending. `Time complexity > O (n log n).` \
  Checking for duplicates. `Time complexity > O(n).` More efficient than brute force.
  - Using Hash Set: Iterate through the array ans store each element within a hash set. \
  If you encounter an element that’s already in the set, you know there’s a duplicate. `Time complexity > O(n)` \
  Most efficient.

### 2. Code Block

Here is the code to check if the array has any element that appears more that once.

```python


```

```javascript


```
