- š Hi, Iām @AmarRich
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
AmarRich/AmarRich is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


class Solution {
public:
    int numSquares(int n) {
        vector<int> dp(n+1); dp[0]=0,dp[1]=1;
        for (int i=2;i<=n;i++){
            int m=INT_MAX;
            for(int j=1;j*j<=i;j++){
                int rem=i-j*j;
                m=min(m,dp[rem]);
            }
               dp[i]=m+1;// +1 previous
        }
        return dp[n];
    }
};
