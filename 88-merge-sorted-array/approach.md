## Approach

To merge two sorted arrays `nums1` and `nums2` into `nums1` in-place, follow this approach:

1. **Use Three Pointers:**  
   - Let `p1` point to the last element in the initial part of `nums1` (`m - 1`).
   - Let `p2` point to the last element in `nums2` (`n - 1`).
   - Let `p` point to the last position in `nums1` (`m + n - 1`).

2. **Merge from the End:**  
   - Compare `nums1[p1]` and `nums2[p2]`.
   - Place the larger value at `nums1[p]`.
   - Move the corresponding pointer (`p1` or `p2`) and decrement `p`.
   - Repeat until either `p1` or `p2` goes below 0.

3. **Copy Remaining Elements:**  
   - If any elements remain in `nums2`, copy them to `nums1` (since `nums1`'s remaining elements are already in place).

This approach ensures all elements are merged in non-decreasing order, and works in O(m + n) time and O(1) extra space.