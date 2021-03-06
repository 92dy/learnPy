列表是一个有序的、可以索引的、线性的、可变的数据结构，使用`[ ]`来表示

## 列表的定义

列表是一个有序序列，用于顺序的存储数据。我们可以通过一下三种方式初始化一个列表

- `L = list()`：使用list函数，定义一个空列表
- `L = list(range(0, 10))`：通过list函数把可迭代对象转换成列表
- `L = []`：使用中括号定义一个空列表
- `L = [1, 2, 3, 4]`

通常在定义列表是使用中括号`[]`,在转换一个可迭代对象伟列表时，使用list函数

### 列表的常见操作

**访问元素**

通过下标来进行访问，索引从0开始；如果下标不存在或报错`IndexError`,负数索引从右边开始，索引从`-1`开始


- `L.index(value, [start, [stop]])`：返回查找范围内的第一个出现该元素的索引
- `L.count(value)`：统计列表中元素出现的个数
- `L.append(object)`：追加一个元素到列表最后,返回`None`
- `L.insert(index, object)`：在指定的索引位置插入一个值，返回`None`
- `L.extend(iterable)`：将一个可迭代对象追加到列表中
- `L.pop([index])`：弹出对应索引上的`Value`,返回`value`
- `L.remove(value)`：删除第一个出现的`value`
- `L.reverse()`：反转列表
- `L.sort(key=None, reverse=False)`：排序
- `L.copy()`：深复制
- `L.clear()`：删除列表元素，使其称为一个空列表
- `del`：删除列表定义

## index的底层实现原理

```
In [  ]: def index(lst, value, start=0, end=-1):
    ...:     i = start
    ...:     for x in lst[start, end]:
    ...:         if x == value:
    ...:             return i
    ...:         i += 1
    ...:     raise ValueError()
```

## count的实现

```
In [  ]: def count(lst, value):
    ...:     c = 0
    ...:     for x in lst:
    ...:         if x == value:
    ...:             c += 1
    ...:     return c

```

## copy详解

对于copy方法来说，copy是一个影子拷贝，修改原列表或者拷贝不会影响被拷贝的列表或者拷贝后的列表;但是这中拷贝只是一层，如果多层则数据就会发生变化

```
In [48]: l1 = [1, 2, 3, ['a', 'b'], 4]

In [49]: l2 = l1.copy()

In [50]: l2
Out[50]: [1, 2, 3, ['a', 'b'], 4]

In [51]: l1[3][0]= 'A'

In [52]: l1
Out[52]: [1, 2, 3, ['A', 'b'], 4]

In [53]: l2
Out[53]: [1, 2, 3, ['A', 'b'], 4]
```

如果不想发生变化，我们可以使用copy模块来实现

```
In [55]: import copy

In [56]: l1 = [1, 2, 3, ['a', 'b'], 4]

In [57]: l2 = copy.deepcopy(l1)

In [58]: l1[3][0]= 'A'

In [59]: l1
Out[59]: [1, 2, 3, ['A', 'b'], 4]

In [60]: l2
Out[60]: [1, 2, 3, ['a', 'b'], 4]
```
