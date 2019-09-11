编写一个函数, 判断一个字符串是否为 IPV4 的地址。

```python
'''
    1.判断字符串是否形如: '192.168.1.1'

   2.字符串两端含有空格视为合法ip，形如: '192.168.1.1'

   3.字符串中间含有空格视为非法ip，形如: '192.168. 1.2'

   4.字符串 '0' 开头视为不合法ip，形如: '192.168.01.1'

   5.字符串 '0.0.0.0' 视为合法ip, '0.0.0.1' 也是
'''

def check_ip(ip):
    ip_segs = ip.split('.')
    if len(ip_segs) != 4:
        return 'ILLEGAL'
    
    ip_strip = ip.strip()
    for item in ip_strip.split('.'):
        if item[0] == ' ':
            return 'ILLEGAL'
        if int(item) < 0 or int(item) > 255:
            return 'ILLEGAL'
        if item[0] == '0' and len(item) != 1:
            return 'ILLEGAL'
        
    return 'LEGAL'
```
