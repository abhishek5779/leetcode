## Approach

To solve the "Product of Array Except Self" problem in O(n) time and without using division, you can use the following approach:

1. **Initialize an output array:**  
   Create an array `answer` of the same length as `nums`. This will store the final result.

2. **Calculate prefix products:**  
   Traverse the array from left to right. For each index `i`, store the product of all elements to the left of `i` in `answer[i]`.  
   - Start with `answer[0] = 1` (since there are no elements to the left of the first element).
   - For each `i` from 1 to n-1:  
     `answer[i] = answer[i-1] * nums[i-1]`

3. **Calculate suffix products and multiply:**  
   Traverse the array from right to left. Keep a variable `R` to store the product of all elements to the right of the current index.  
   - Start with `R = 1` (since there are no elements to the right of the last element).
   - For each `i` from n-1 to 0:  
     - Multiply `answer[i]` by `R`.
     - Update `R = R * nums[i]`.

This way, `answer[i]` will contain the product of all elements except `nums[i]`, using only O(1) extra space (excluding the output array).

### Example

For `nums = [1,2,3,4]`:

- Prefix pass: `answer = [1, 1, 2, 6]`
- Suffix pass (with R):  
  - i=3: answer[3] *= 1 → 6, R = 4  
  - i=2: answer[2] *= 4 → 8, R = 12  
  - i=1: answer[1] *= 12 → 12, R = 24  
  - i=0: answer[0] *= 24 → 24

Final output: `[24, 12, 8, 6]`