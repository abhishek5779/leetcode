# Approach to Solve "Binary Search"

## Understand the Problem:
You are given a sorted array `nums` and a target value `target`.  
The task is to find the index of `target` in `nums`. If `target` does not exist, return `-1`.  
The solution must have a time complexity of **O(log n)**, which suggests using the binary search algorithm.

## Plan the Solution:
Use the **binary search algorithm**:
1. Initialize two pointers: `left` (start of the array) and `right` (end of the array).
2. While `left` is less than or equal to `right`:
   - Calculate the middle index: `mid = left + (right - left) / 2`.
   - Compare `nums[mid]` with `target`:
     - If `nums[mid] == target`, return `mid`.
     - If `nums[mid] < target`, move the `left` pointer to `mid + 1`.
     - If `nums[mid] > target`, move the `right` pointer to `mid - 1`.
3. If the loop ends without finding the target, return `-1`.

## Complexity Analysis:
### Time Complexity:
- **O(log n)**: The search space is halved at each step.

### Space Complexity:
- **O(1)**: No additional data structures are used.