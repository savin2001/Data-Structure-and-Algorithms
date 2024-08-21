# Duplicate Integer (Easy)

Given an integer array nums, return true if any value appears more than once in the array, otherwise return false.

## Example 1

```javascript
Input: let nums = [1, 2, 3, 3]

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
  - Using Hash Set: Iterate through the array and store each element within a hash set. \
  If you encounter an element that’s already in the set, you know there’s a duplicate. `Time complexity > O(n)` \
  Most efficient. `I am yet to learn this method (12-Aug-2024)` > `Finally learnt this method (21-Aug-2024)` 

### 2. Code Block

Here is the code to check if the array has any element that appears more that once.

#### 2.1 Using Hash Set

Here is solution:
```javascript
// JavaScript
var containsDuplicate = function(nums) {
    // Convert the array into a Set, which automatically removes any duplicates.
    // Check if the size of the Set (number of unique elements) is not equal to 
    // the total number of elements in the original array. If they are not equal, 
    // it means there were duplicates in the array.
    return new Set(nums).size !== nums.length;
};

const numbers = [1, 2, 3, 4, 5, 1];
console.log(containsDuplicate(numbers)); // Output: true
```
```python

```

#### 2.2 Sorting Array

Here is solution:
```javascript
    // JavaScript
    class Solution {
        /**
         * @param {number[]} nums
         * @return {boolean}
         */
    
        hasDuplicate(nums) {
            // Check if the array is empty or has only 1 element
            if (nums.length <= 1) {
                return false;
            }
        
            // Sort the array
            let newArray = nums.sort((a, b) => a - b);

            // Loop through the array to get the elements
            for (let i = 0; i < newArray.length - 1; i++) {
                // Compare if the adjacent values of the array are equal
                if (newArray[i] === newArray[i + 1]) {
                    return true; // Duplicate found
                }
            }

            // No duplicates found
            return false;
        }
    }

    // Example:
    let solution = new Solution();
    let numbers = [1, 2, 3, 4];
    console.log(solution.hasDuplicate(numbers)); // The expected output: false

    numbers = [1, 2, 3, 1];
    console.log(solution.hasDuplicate(numbers)); // The expected output: true

```
```python

```
