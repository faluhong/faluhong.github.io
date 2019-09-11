写一个栈，可以查长度，可以添加、删除元素？

```python
class Stack(object):
    """栈"""
    def __init__(self):
        """初始化"""
        self.__list = []      # 定义一个列表用于存放数据

    def push(self, data):
        """添加一个新的元素data到栈顶"""
        self.__list.append(data)    # 把列表的尾部作为栈顶

    def pop(self):
        """弹出栈顶元素"""
        return self.__list.pop()    # 从列表尾部出栈操作

    """
        也可以把列表头部作为栈顶,如果把列表头部作为栈顶，
        则压栈就是 self.__list.insert(0, data),
        出栈则是self.__list.pop(0)
        此种方式与把列表尾部作为栈顶区别在于，列表尾部操作时间复杂度是O（1），而头部操作时间复杂度是O（n）
    """
    def peek(self):
        """返回栈顶元素"""
        if self.__list:           # 列表为空时，返回None，否则返回最后一个元素
            return self.__list[-1]
        else:
            return None

    def is_empty(self):
        """判断栈是否为空"""
        return not self.__list    # 列表为空时，返回True，否则返回False

    def size(self):
        """返回栈的元素个数"""
        return len(self.__list)

if __name__ == '__main__':
    s = Stack()
    s.push(1)
    s.push(2)
    s.push(3)
    s.push(4)
    print("栈顶数据：", s.peek())
    print("判空：", s.is_empty())
    print("长度：", s.size())

    print(s.pop())
    print(s.pop())
    print(s.pop())
    print(s.pop())
    print("栈顶数据：", s.peek())
    print("判空：", s.is_empty())
    print("长度：", s.size())
```

