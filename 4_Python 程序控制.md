#### 顺序

按照先后顺序一条条执行

#### 分支

根据不同情况判断，条件满足执行某条件下的语句

- **单分支结构**

```
if 1<2:
    print('1 less than 2')
```

- **多分支结构**

```
score = int(input("Please Enter a num>>>: "))

if score>=90:
    print('A++')
elif 70<=score<80:
    print('B++')
elif 60<=socre<70:
    print('C')
else:
    print('D')
```



#### 循环

条件满足就反复执行，不满足就不执行或不再执行

- **while语句**：当条件满足时，进入循环体

```
flag = 10
while flag:
    print(flag)
    flag -= 1
```

- **for语句**：当可迭代对象中元素可以迭代时，进入循环体

```
for i in range(10):
    print(i)
```

- **continue语句**：中断当前的当次循环，继续下一次循环

```
for i in range(5):
    if i == 3:
        continue
    print(i)
0
1
2
4
```

- **break语句**：终止当前循环

```
for i in range(5):
    if i == 3:
        break
    print(i)
0
1
2
```

- **else子句**：如果循环正常结束，就执行else语句，如果使用break终止，else子句不会执行

```
a = 5
while a > 0:
    print(a)
    a -= 1
else:
    print('end of print')
》》
  5
  4
  3
  2
  1
  end of print
```
```
a = 5
while a > 0:
    print(a)
    a -= 1
    break
else:
    print('end of print')
》》
  5
```
