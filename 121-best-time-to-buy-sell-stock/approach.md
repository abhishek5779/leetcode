# Approach

## Understand the Problem:
You are given an array `prices` where `prices[i]` represents the price of a stock on the `i`th day.  
The goal is to find the maximum profit by choosing a single day to buy and a different day in the future to sell.  
If no profit can be made, return `0`.

## Plan the Solution:
- Use a single pass approach to find the maximum profit:
  - Keep track of the minimum price encountered so far while iterating through the array.
  - For each price, calculate the potential profit by subtracting the minimum price from the current price.
  - Update the maximum profit if the calculated profit is greater than the current maximum profit.

## Complexity Analysis:
### Time Complexity:
- **O(n)**, where `n` is the length of the `prices` array. The array is traversed once.

### Space Complexity:
- **O(1)**, as no additional data structures are used.