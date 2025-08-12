```cpp
class Solution {
public:
    bool isValid(string s) {
        unordered_map <char, char> constant = {{')','('}, {'}','{'}, {']', '['}};
        stack <char> store;
        int length = s.size();
        for(int i=0;i<length;i++)
        {
            if(s[i]=='(' || s[i]=='{' || s[i]=='[')
                store.push(s[i]);
            else 
            {
                if(store.empty() || constant[s[i]]!=store.top())
                    return false;
                store.pop();
            }
        }
        return store.empty(); 
    }
};
```
