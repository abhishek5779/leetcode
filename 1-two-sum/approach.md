## Approach

1. **Understand the Problem**:
   - You need to find two numbers in the array that add up to the given target.
   - Each input will have exactly one solution, and you cannot use the same element twice.

2. **Brute Force Approach**:
   - Use two nested loops to check every pair of numbers.
   - This approach has a time complexity of O(n^2), which is not efficient for large arrays.

3. **Optimized Approach Using Hash Map**:
   - Use a hash map to store the difference between the target and each element as you iterate through the array.
   - For each element, check if the difference is already in the hash map.
   - If it is, you have found the two numbers that add up to the target.
   - This approach has a time complexity of O(n), which is more efficient.

3. **Two pointer approach**:
   - Sort the array and use two pointer iterating the array, one from start and other from end.
   - Calculate the sum and if it's less than target then increament the start pointer and if it's greater than target then decrease the end pointer.
   - Iterate this until you find the sum equals to the target.
   - This approach is optimal when you only have to check whether two such elements exist or not. But if you have to return the index of those elements then it's not the optimal approach.

**Detailed Explanation** - https://www.youtube.com/watch?v=UXDSeD9mN-k 