## Approach

1. **Understand the Problem**:
   - You need to move all zeroes in the array to the end while maintaining the order of non-zero elements.
   - This must be done in-place, meaning you cannot use extra space for another array.

2. **Initialize Pointers**:
   - Use a pointer `start` to keep track of the position where the next non-zero element should be placed.

3. **First Pass - Move Non-Zero Elements**:
   - Iterate through the array using a for loop.
   - For each element, if it is not zero, move it to the position indicated by `start` and increment `start`.

4. **Second Pass - Fill Remaining Positions with Zeroes**:
   - After all non-zero elements have been moved to the beginning of the array, fill the remaining positions with zeroes.

5. **In-Place Operation**:
   - Ensure that the entire operation is done in-place without using any additional arrays, ensuring that the space complexity is O(1).