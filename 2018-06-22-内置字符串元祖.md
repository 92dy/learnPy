## 元祖的定义

元祖是不可变的，它可以通过一下方式进行初始化：

- `t = tuple()`
- `t = tuple(range(5))`
- `t = ()`
- `t = (1, )`
- `t = (1, 2, 3)`

## 元祖的操作

**查询元祖**

- `t[0]`：下标操作
- `T.count(value)`：统计元素的个数
- `T.index(value, [start, [stop]])`：根据值查找索引

## 命名元祖

我们有时会使用命名元祖，命名元祖从标准模块中导入，主要为了便于引用，见名知意。

```
In [66]: from collections import namedtuple

In [67]: user = namedtuple('user', ['name', 'age'])

In [68]: me = user('rex', 24)

In [69]: me.name
Out[69]: 'rex'

In [70]: me.age
Out[70]: 24
```
