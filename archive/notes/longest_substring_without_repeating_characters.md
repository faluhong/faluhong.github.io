给定一个字符串，找出不含有重复字符的**最长子串**的长度。

**示例 1:**

```
输入: "abcabcbb"
输出: 3 
解释: 无重复字符的最长子串是 "abc"，其长度为 3。
```

**示例 2:**

```
输入: "bbbbb"
输出: 1
解释: 无重复字符的最长子串是 "b"，其长度为 1。
```

**示例 3:**

```
输入: "pwwkew"
输出: 3
解释: 无重复字符的最长子串是 "wke"，其长度为 3。
     请注意，答案必须是一个子串，"pwke" 是一个子序列 而不是子串。
```



### 思路

考虑字符串：`abcabcbb`，从第 0 个字符 `a` 开始，然后是第 1 个字符 `b`，发现 `b` 不在 `a`（我这里用 `s_sub_new` 来存储） 中，于是，将字符 `b` 添加到 `a` 中，也就是 `s_sub_new` 中，这时候 `s_sub_new` 变成了 `ab`。然后接着就是第 2 个字符 `c` 了，发现 `c` 也不在 `s_sub_new`（`ab`）中，于是将 `c` 添加到 `s_sub_new` 中。

接着就是第 3 个字符 `a` 了，这时候发现，在前面已经存储的 `s_sub_new` 中，为 `abc`，已经有了字符 `a` 了，这时候，将前面的字符串 `abc` 中，我们去掉 `a`，保留字符 `a` 之后的字符串，为 `bc`，将第 3 个字符 `a` 添加到 `bc` 上，组成新的字符串 `bca`，以此类推。

为了防止 `s_sub_new` 中的字符串长度“变短”，我们需要一个 `s_sub_old` 来记录历史上曾经出现过的最长的字符串。

还要考虑到字符串长度为 1 的情况，这时候，直接返回 1。



### 解答

```python
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        """
        :type s: str
        :rtype: int
        """
        
        # 考虑到字符串长度为 1 的情况
        if len(s) == 1:
            return 1
        
        s_sub_old = ''
        s_sub_new = ''
        
        for i, char in enumerate(s):
            pos = s_sub_new.find(char)
            if pos == -1:
                s_sub_new += char
            else:
                if len(s_sub_new) >= len(s_sub_old):
                    s_sub_old = s_sub_new
                s_sub_new = s_sub_new[(pos + 1):] + char
        
        if len(s_sub_new) >= len(s_sub_old):
            return len(s_sub_new)
        else:
             return len(s_sub_old)
```

