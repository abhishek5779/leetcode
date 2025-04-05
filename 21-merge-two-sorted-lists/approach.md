# Approach to Solve "Merge Two Sorted Lists"

To solve the "Merge Two Sorted Lists" problem, a person should approach it systematically as follows:

## 1. Understand the Problem
You are given two sorted linked lists, `list1` and `list2`.  
The task is to merge these two lists into a single sorted linked list.  
The merged list should be created by splicing together the nodes of the two input lists.  
Return the head of the merged linked list.

## 2. Plan the Solution
- Use a **two-pointer approach** to traverse both lists simultaneously.
- Create a dummy node to simplify the merging process and maintain a pointer (`current`) to build the merged list.
- Compare the current nodes of `list1` and `list2`:
  - Append the smaller node to the merged list and move the pointer of the corresponding list forward.
- If one of the lists is exhausted, append the remaining nodes of the other list to the merged list.
- Return the merged list starting from the node after the dummy node.

## 3. Optimize
- The solution has a time complexity of **O(n + m)**, where `n` and `m` are the lengths of `list1` and `list2`, as each node is processed once.
- The space complexity is **O(1)**, as the merging is done in-place without using additional memory.

By following this structured approach, the problem can be solved efficiently and correctly.