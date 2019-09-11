两个整数之间的[汉明距离](https://baike.baidu.com/item/%E6%B1%89%E6%98%8E%E8%B7%9D%E7%A6%BB)指的是这两个数字对应二进制位不同的位置的数目。

给出两个整数 `x` 和 `y`，计算它们之间的汉明距离。

**注意：**
0 ≤ `x`, `y` < 231.

**示例:**

```
输入: x = 1, y = 4

输出: 2

解释:
1   (0 0 0 1)
4   (0 1 0 0)
       ↑   ↑

上面的箭头指出了对应二进制位不同的位置。
```



```python
class Solution(object):
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        x_b = "{0:b}".format(x)
        y_b = "{0:b}".format(y)
        
        cnt = 0
        
        if len(x_b) >= len(y_b):
            tmp_max = x_b
            tmp_min = y_b
        else:
            tmp_max = y_b
            tmp_min = x_b
        
        for i in range(len(tmp_max)):
            if i <= len(tmp_min) - 1:
                if tmp_max[-(i+1)] != tmp_min[-(i+1)]:
                    cnt += 1
            else:
                if tmp_max[-(i+1)] != '0':
                    cnt += 1
            
        return cnt
```



```python
class Solution(object):
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        return  bin(x^y).count('1')
    
    
    
#         h1 = format(2**31 + x, 'b')
#         h2 = format(2**31 + y, 'b')
#         count = 0
#         for i in range(1, max(len(format(x,'b')), len(format(y,'b'))) + 1):
#             if h2[-i] != h1[-i]:
#                 count += 1
#         return count 
```

