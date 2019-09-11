给定字符串`J` 代表石头中宝石的类型，和字符串 `S`代表你拥有的石头。 `S` 中每个字符代表了一种你拥有的石头的类型，你想知道你拥有的石头中有多少是宝石。

`J` 中的字母不重复，`J` 和 `S`中的所有字符都是字母。字母区分大小写，因此`"a"`和`"A"`是不同类型的石头。



```python
输入: J = "aA", S = "aAAbbbb"
输出: 3
```



```python
输入: J = "z", S = "ZZ"
输出: 0
```



```python
class Solution(object):
    def numJewelsInStones(self, J, S):
        """
        :type J: str
        :type S: str
        :rtype: int
        """
        cnt = 0
        for s in S:
            if s in J:
               cnt += 1
            
        return cnt
```

