# DP problems
- Fibonacci
  - Recursion  
    fib(n)=fib(n-1)+fib(n-2);  
  - DP  
    dp[0]=1,dp[1]=1;  
    dp[i]=dp[i-1]+dp[i-2];  
- 0/1 Knapsack
  - Recursion  
    if(n==0||W==0)
      &emsp;return 0;  
    if(weight[n-1]>W)  
    {  
      &emsp;return knapsack(val[],weight[],n-1,W);  
    }  
    else  
    {  
      &emsp;return max(knapsack(val[],weight[],n-1,W),val[n-1]+knapsack(val[],weight[],n-1,W-weight[n-1]));    
    }
  - DP  
    Initialize first row and column with 0s  
    if (weight[i-1]>j)  
    {  
      &emsp;dp[i][j]=dp[i-1][j];    
    }  
    else  
    {  
      &emsp;dp[i][j]=max(dp[i-1][j],val[i-1]+dp[i-1][j-weight[i-1]];    
    }  
  - Variations
    - [Subset Sum](https://www.geeksforgeeks.org/subset-sum-problem-dp-25/)  
      - Initialize first row with false and first column with true  
      - Pseudocode-  
        if (arr[i]>j)  
        {  
          &emsp;dp[i][j]=dp[i-1][j];  
        }  
        else  
        {  
          &emsp;dp[i][j]=dp[i-1][j] || dp[i-1][j-arr[i-1]];  
        }
    - Equal sum partition
      - if (sum of all array elements is odd) return false  
      - else solve subset sum for (sum of all array elements/2)
    - [Count of subsets with a given sum](https://www.geeksforgeeks.org/count-of-subsets-with-sum-equal-to-x/)  
      - Initialize first row with 0 and first column with 1   
        if (arr[i]>j)  
        {  
          &emsp;dp[i][j]=dp[i-1][j];  
        }  
        else  
        {  
          &emsp;dp[i][j]=dp[i-1][j] + dp[i-1][j-arr[i-1]];  
        }
    - Minimum Subset Sum Difference
      - Sum of all array elements is S1 + S2 = SUM
      - Min difference to find is S2-S1
      - Min difference is SUM - 2S1
      - Maximize S1 such that SUM-2S1 remains greater than 0
      - Solve Subset sum and find first subset sum less than SUM/2 and store in S1
      - Return SUM-2S1

  
- Unbounded Knapsack
  - Recursion
  - DP  
    Initialize first row and column with 0s  
    if (weight[i]>j)  
    {  
      &emsp;dp[i][j]=dp[i-1][j]  
    }  
    else  
    {  
      &emsp;dp[i][j]=max(dp[i-1][j],val[i-1]+dp[i][j-weight[i]]  
    }  
  - Variations
 
- Longest Common Subsequence
  - Recursion-
    if(n==0||m==0)
      &emsp;return 0;  
    if(X[m-1]==Y[n-1])  
    {  
      &emsp;return 1+LCS(X[],Y[],m-1,n-1);  
    }  
    else  
    {  
      &emsp;return max(LCS(X[],Y[],m,n-1),LCS(X[],Y[],m-1,n);    
    }
  - DP-
    Initialize first row and column with 0s  
    if(X[i-1]==Y[j-1])  
    {  
      &emsp;dp[i][j]=1+dp[i-1][j-1];  
    }  
    else  
    {  
      &emsp;dp[i][j]=max(dp[i-1][j],dp[i][j-1]);    
    }  
  - Variations
    - Longest Common Substring
- Matrix Chain Multiplication
