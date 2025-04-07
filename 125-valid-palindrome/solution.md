```cpp
class Solution {
public:
    bool isPalindrome(string s) {
        vector <char> palindrome;
        int stringlength=s.size();
        for(int i=0;i<stringlength;i++)
        {
            if(s[i]>=65 && s[i]<=90) //Covers Uppercase alphabets
                palindrome.push_back(s[i]+32);
            if(s[i]>=97 && s[i]<=122) //Covers lowercase alphabets
                palindrome.push_back(s[i]);
            if(s[i]>=48 && s[i]<=57) //Covers numeric values
                palindrome.push_back(s[i]);
        }
        int n=palindrome.size();
        for(int i=0,j=n-1;i<j;i++,j--)
        {
            if(palindrome[i]!=palindrome[j])
                return false;
        }
        return true;
        
    }
};
```

## Below solution is with O(1) space complexity

```cpp
class Solution {
public:
    bool alphanum(char c)
    {
        if((c>=97 && c<=122) || (c>=65 && c<=90) || (c>=48 && c<=57))
            return true;
        return false;
    }
    bool isPalindrome(string s) {
        vector <char> palindrome;
        int stringlength=s.size();
        int i=0;
        int j=stringlength-1;
        while(i<j)
        {
            while(i<j && !alphanum(s[i]))
                i++;
            while(i<j && !alphanum(s[j]))
                j--;
            
            if(alphanum(s[i]) && alphanum(s[j]))
            {
                if((s[i]>=65 && s[i]<=90))
                    s[i]=s[i]+32;
                if((s[j]>=65 && s[j]<=90))
                    s[j]=s[j]+32;
                if(s[i]!=s[j])
                    return false;
                i++;
                j--;
            }
            
        }
        return true;
        
    }
};
```