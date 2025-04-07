```cpp
class Solution {
public:
    bool isAnagram(string s, string t) {
        if(s.size()!=t.size())
            return false;

        int first[26]={0};
        int second[26]={0};
        for(int i=0;i<s.size();i++)
            first[s[i]-'a']++;
        for(int i=0;i<t.size();i++)
            second[t[i]-'a']++;
        for(int i=0;i<26;i++)
        {
            if(first[i]!=second[i])
                    return false;
        }
        return true;
    }
};
```