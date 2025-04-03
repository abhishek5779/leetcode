```cpp
class Solution {
public:
    bool isValid(string s) {
        stack <char> store;
        int size = s.length();
        for(int i=0;i<size;i++)
        {
            if (s[i] == '(' || s[i] == '[' || s[i] == '{' )
                store.push(s[i]);
            else
            {

                if(s[i] == ')')
                {
                    if(!store.empty() && store.top() == '(')
                        store.pop();
                    else
                        return false; 
                }
                if(s[i] == ']')
                {
                    if(!store.empty() && store.top() == '[')
                        store.pop();
                    else
                        return false; 
                }
                if(s[i] == '}')
                {
                    if(!store.empty() && store.top() == '{')
                        store.pop();
                    else
                        return false; 
                }
            }
        }
        if(store.empty())
            return true;
        else
            return false;
    }
};
```