# Approach to Solve "Linked List Cycle"

To solve the "Linked List Cycle" problem, a person should approach it systematically as follows:

## 1. Understand the Problem
You are given the head of a linked list.  
The task is to determine if the linked list contains a cycle.  
A cycle exists if a node in the list can be revisited by continuously following the `next` pointer.  
The `pos` parameter indicates the index of the node where the cycle begins (if it exists). If `pos = -1`, there is no cycle.

## 2. Plan the Solution
Use the **Floyd's Cycle Detection Algorithm (Tortoise and Hare)**:
- Use two pointers, `slow` and `fast`.
- Initialize both pointers to the head of the linked list.
- Move `slow` one step at a time and `fast` two steps at a time.
- If there is a cycle, the `slow` and `fast` pointers will eventually meet.
- If `fast` or `fast.next` becomes `None`, the list does not contain a cycle.

## 3. Optimize
- The solution has a time complexity of **O(n)**, where `n` is the number of nodes in the linked list, as each node is visited at most once.
- The space complexity is **O(1)**, as no additional data structures are used.

By following this structured approach, the problem can be solved efficiently and correctly.