```cpp
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int n=prices.size();
        int min=prices[0];
        int profit=0;
        for(int i=1;i<n;i++)
        {
            if(prices[i]<min)
                min=prices[i];
            int sub=prices[i]-min;
            if(sub>profit)
                profit=sub;
        }
        return profit;
    }
};
```