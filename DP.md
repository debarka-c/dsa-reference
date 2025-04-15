# DP problems
- 0/1 Knapsack
  - Recursion
  - DP  
    Initialize first row and column with 0s  
    if (weight[i]>j)  
    {  
      &emsp;dp[i][j]=dp[i-1][j]  
    }  
    else  
    {  
      &emsp;dp[i][j]=max(dp[i-1][j],dp[i-1][j-weight[i]]  
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
          &emsp;dp[i][j]=dp[i-1][j] || dp[i-1][j-arr[i]];  
        }
    - Equal Sum Partition
      - if (sum of all array elements is odd) return false  
      - else solve subset sum for (sum of all array elements/2)
    - Count of Subsets with a Given Sum  
      - Initialize first row with 0 and first column with 1  
      - Pseudocode-  
        if (arr[i]>j)  
        {  
          &emsp;dp[i][j]=dp[i-1][j];  
        }  
        else  
        {  
          &emsp;dp[i][j]=dp[i-1][j] + dp[i-1][j-arr[i]];  
        }
    - Minimum Subset Sum Difference
      - Initialize
      - Sum of all array elements is S1 + S2
      - Difference to find is S2-S1
      - Difference is Sum - 2S1
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
      &emsp;dp[i][j]=max(dp[i-1][j],dp[i][j-weight[i]]  
    }  
  - Variations
- Matrix Chain Multiplication
