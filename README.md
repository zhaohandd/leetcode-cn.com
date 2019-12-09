# leetcode-cn.com
给自己看的leetcode刷题记录

## 动态规划
### 5. 最长回文子串
```
class Solution {
    public String longestPalindrome(String s) {
        String result = "";
        int length = s.length();
        // 动态规划，双指针
        boolean dp[][] = new boolean[length][length];
        for (int i = 0; i < length; i++) {
            for (int j = i; j >=0; j-- ) {
                if (s.charAt(i) == s.charAt(j) && (i-j<2 || dp[i-1][j+1])) {
                    dp[i][j] = true;
                }
                if (dp[i][j] && (i-j+1 > result.length())) {
                    result = s.substring(j, i+1);
                }
            }
        }
        return result;
    }
}
```
### 53. 最大子序和
```
class Solution {
    public int maxSubArray(int[] nums) {
        int result = nums[0];
        int sum = 0;
        for (int num : nums) {
            if (sum > 0) {
                sum += num;
            } else {
                sum = num;
            }
            result = Math.max(result, sum);
        }
        return result;
    }
}
```
### 85. 最大矩形
### 10. 正则表达式匹配
### 95. 不同的二叉搜索树
### 351. 安卓系统手势解锁
### 72. 编辑距离
### 96. 不同的二叉搜索树
### 70. 爬楼梯
### 818. 赛程
### 312. 戳气球
### 64. 最小路径和
### 121. 买卖股票的最佳时机
## 堆

## 二叉树

## 二分查找

## 广度优先搜索

## 深度优先搜索

## 哈希表

## 回溯算法

## 链表

## 设计

## 数学

## 数组

## 贪心算法

## 位运算

## 字符串
