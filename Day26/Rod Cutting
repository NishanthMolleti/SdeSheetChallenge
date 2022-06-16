	int solve(vector<int> &price, int idx, int N, vector<vector<int>> &dp)
    {
        if(idx == 0)
            return N*price[0];
        if(dp[idx][N] != -1) return dp[idx][N];
        
        int notTake = 0 + solve(price, idx-1, N, dp);
        int take = INT_MIN;
        int rodLen = idx+1;
        if(rodLen <= N) 
            take = price[idx] + solve(price, idx, N-rodLen, dp);
        
        return dp[idx][N] = max(take, notTake);
        
    }
    int cutRod(vector<int> &price, int n)
    {
        vector<vector<int>> dp(n, vector<int>(n+1, -1));
        return solve(price, n-1, n, dp);   
    }
