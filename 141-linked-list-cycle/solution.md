```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
 #include <map>
class Solution {
public:
    bool hasCycle(ListNode *head) {
        if(head==NULL || head->next==NULL)
            return false;
        ListNode* jump=head;
        ListNode* single=head;
        while(jump!=NULL && jump->next!=NULL)
        {
            single=single->next;
            jump=jump->next->next;
            if(single==jump)
                return true;
        }
        return false;
    }
};
```