py3 引进两个新的类型
- `bytes`：不可变字节序列
- `bytearray`：可变字节数组

#### 字符串与bytes

字符串是`字符`组成的有序序列，字符可以用编码来理解
bytes是`字节`组成的有序的`不可变`序列
bytearray是`字节`组成的有序的`可变`序列

#### 编码与解码

字符串按照不同的字符集编码`encode`返回字节序列bytes
- `encode(encoding='utf-8', errors='strict')` --> `bytes`

字节序列安装不同的字符集解码`decode`返回字符串
- `decode(encoding='utf-8', errors='strict')` --> `str`

#### bytes定义

- 空bytes：`bytes()`
- 指定自己的bytes，被0填充：`bytes(int)`
- bytes[0,255]的int组成的可迭代对象：`bytes(iteable_of_ints)`
- bytes等价于string.encode()：`bytes(string, encoding[, errors])`
- 从一个字节序列或者buffer赋值处一个心底的不可变的bytes对象：`bytes(bytes_or_buffer)`

### 11-57
