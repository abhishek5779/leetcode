## Example Code

```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> num_map; // To store the difference and index
        for (int i = 0; i < nums.size(); i++) {
            int complement = target - nums[i];
            if (num_map.find(complement) != num_map.end()) {
                return {num_map[complement], i}; // Return the indices of the two numbers
            }
            num_map[nums[i]] = i; // Store the index of the current element
        }
        return {}; // Return an empty vector if no solution is found
    }
};