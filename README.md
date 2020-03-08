# Longest Common Prefix
# https://leetcode.com/problems/longest-common-prefix

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string "".
```
Example 1:

Input: ["flower","flow","flight"]
Output: "fl"

Example 2:

Input: ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.
```
**Note:**
All given inputs are in lowercase letters a-z.


# Implementation :

```java
class Solution {
    public String longestCommonPrefix(String[] strs) {
        if(strs == null || strs.length == 0)
            return "";
            
        String longestCommonPrefix = "";
        for(int i = 0; i < strs[0].length(); i++){
            for(int j = 1; j < strs.length; j++){
                if(strs[j].length() <= i || strs[0].charAt(i) != strs[j].charAt(i))
                    return longestCommonPrefix;
            }
            longestCommonPrefix += strs[0].charAt(i);
        }
        return longestCommonPrefix;
    }
}
```

# References :
1. https://www.youtube.com/watch?v=1YQmI7F9dJ0
2. https://www.youtube.com/watch?v=bl8ue-dTxgs
3. https://leetcode.com/articles/longest-common-prefix
