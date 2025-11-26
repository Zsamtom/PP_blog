[TOC]

### 1 变量

计算机中的存储空间，用于保存数据

```python
定义变量的格式
变量名 = 值
注意：= 是赋值运算符，左右两边打上空格是为了代码的规范性，美观性。
```

```python
numl = 3  #numl就是一个变量，保存可乐的价格
num2 = 10   #num2也是一个变量，保存冰淇淋的价格
total= num1 + num2 #total也是一个变量，保存总价格

a = 999	# 一个变量可以反复赋值,并且可以是不同的数据类型
```

```python
print (numl)
# 加上引号会打印引号里面的内容，没有引号就会被识别成变量名，打印的是变量的值，如果该变量没有被赋值，就会报命名错误
变量只有再赋值以后才会被创建，所以使用变量之前必须要赋值
```

`注意事项：首次使用变量会在内存中划分空间，并初始化值再次使用变量不再划分空间修改原空间的值。`

### 2 标识符

含义：程序员定义变量名、函数名

` 标识符规定：
1.只能由数字、字母、_(下划线)组成
2.不能以数字开头
3.不能是关键字
4.严格区分大小写`

```python
关键字：是python中已经使用了的标识符，具有特殊的功能和含义。
['False','None','True','and','as','assert','async','await', 'break','class','continue','def','del′,‘elif','else','except','finally’,‘for’,‘from’，‘global’，‘if,‘import','in','is','lambda','nonlocal','not','or','pass’,‘raise′,'return','try','while','with','yield']
```

```python
1.见名知义
2.下划线分割法：
多个单词组成的名称，使用小写字母，单词与单词之间使用下划线分开。
3.大驼峰命名法：
多个单词组成的名称，每个单词的首字母大写，其余字母小写。
4.小驼峰命名法：
第一个单词首字母小写，后面单词首字母大写，其余字母小写。
```

### 3 数据类型

**int整型**

int整型（常用）：任意大小的整数

```python
num = 1000
检测数据类型的方法
print(type (num))
```

**浮点型**

小数

**布尔型**

有固定写法，一个为True（真），一个为False（假）

必须严格区分大小写

布尔值可以当作整型对待，True相当于整数1，False相当于整数0

**comple复数**

```python
固定写法：z = a + bj
```

**字符串**

特点：需要加上引号，单引号和双引号都可以，包含了多行内容的时候也可以使用三引号

--注意多行注释和用三引号的字符串类型的区别，多行注释是单独存在的，前面不需要变量名--

**占位符**

占位符的作用：生成一定格式的字符串
占位符的三种方式
`1 %
2 format（） 
3 格式化f`

%s 字符串（常用）
%d 整数（常用）
%4d 整数
数字设置位数，不足前面补空白

```python
name ='bingbing'
print("我的名字：%s” % name)
# 注意：占位符只是占据位置，并不会被输出
      
age = 18
name ='bingHing"
print（"我的名字:%s，年龄：%d” %（name,age))

a = 123
print("%05d" % a)
--> 00123
表示输出的整数显示位数，不足的话用0补全，超出当前位数则原样输出
```

**%f 浮点数（常用）**

```python
a = 1. 2345673 
print ("%f" % a)
# 默认后六位小数，遵循四舍五入原则

b = 2.34567
print ("%.3f" % b)
--> 2.346

```

```python
%%
print(“我是%%的1%%” %())
--> 我是%的1%
```

**f 格式化**

```python
name = "nigning"
#格式：f"{表达式}“e='bingbing
age = 18
print(f"我的名字是{name}，我今年{age}岁了")
--> 我的名字是nigning，我今年18岁了
```

![image-20251108223806909](C:\Users\皮\AppData\Roaming\Typora\typora-user-images\image-20251108223806909.png)

### 4 运算符

#### 4.1算数运算符

`+ - * /`   注意：使用算术运算符/，商一定是浮点数

`//`    //取整除取商的整数部分，向下取整 向下取整：不管四舍五入的规则，只要后面有小数，就忽略小数
			`print（7.0//2）`使用算术运算符，其中若有浮点数，结果也会用浮点数表示

`%` 	%取余数只取余数部分

`**`	\**幕  m**n：m的n次方

#### 4.2 赋值运算符

`=`

- 将运算的值赋给变量
- 将一个变量的值赋给另外一个变量
- 给变量赋值

`+= `	等效于左边变量的值加上右边变量的值并赋给左边的值

`-=`	等效于左边变量的值减去右边变量的值并赋给左边的值

`/=    *=`

#### 4.3 比较运算符

`==`	比较的是两个变量的值是否相等，相等的话就返回为True（真），不相等返回为False（假）

`!=`	比较的是两个变量的值是否相等，不相等的话就返回为True（真），相等返回为False（假）

`<  > <= >=` 

#### 4.4 逻辑运算符

`and`	左石两边都符合才为真

`or`	只需要一边符合就为真

`not`	表示相反的结果

#### 4.5 三目运算（三元表达式）

基本格式：为真结果 if 判断条件 else 为假结果

`print("a小于等于b"） if a<=b else print("a比b大")`

###  5 输入函数 input（）

prompt是提示，会在控制台中显示 input (prompt)    默认输入的是字符串

```python
name = input（"请输入姓名:")
print (name)
pwd =input（"请输入你的密码：")
print (pwd)
```

### 6 转义字符

`\t` 制表符通常表示空四个字符，也称缩进

`\n` 换行符 表示将当前位置移到下一行开头 [`print()` 会空一行`print(end = '\n') ` 会空一行`print('\n')`会空两行 `print(end='')`不会换行继续在当前行输出]

`\r` 回车表示将当前位置移到本行开头（前面的就没了）

`\\` 反斜杠符号     `print(r'sixs\\\\tar')`  r 原生字符串，默认取消转义

### 7 if判断

基本格式 	if 要判断的条件：条件成立的时候要做的事情（冒号和缩进需要注意）

`if-else`

```python
基本格式：
if 条件：
   满足条件时要做的事情
else:    #else后面不需要添加任何条件
   不满足条件时要做的事情
```

`if-elif` `if-elif-else`   可以写很多个elif

```python
if 条件1:
    满足条件1要做的事情
elif 条件2:
    满足条件2要做的事情
elif 条件3:
    满足条件3要做的事情
else:
    所有条件都不符合的输出
```

`if嵌套`  
**含义**：if里面有if
**注意**：外层的if判断，也可以是if-else;
         内层的if判断， 也可以是if-else。

```python
格式：
if 条件1 :
   事情1
   if 条件2 :
     事情2
else:
   不满足条件的事情
```

```python
#定义一个布尔型变量，表示是否有车票
#True代表有车票，False代表没车票
ticket = True
temp = 36.5
#判断是否有车票
if ticket == True:	#外层if判断
    print（"可以进站了哈哈哈-->"end=""） #正常人腋下体温是36.3-37.2
    if 36.3 <= temp <= 37.2:
        print（"体温正常，安心回家")
    else:
        print（"体温异常，被抓过去隔离")
else:
    print（"没票不能进站")
```

### 8 循环语句

#### while循环

```python
基本语法：
定义初始变量
while 条件：
     循环体
     改变变量
```

如果没有改变变量，条件一直满足，就会一直环下去，一直执行

```python
# 死循环
while True(1 2....):   # 条件只写True，说明一直为真，就会一直执行，从而形成一个死循环
      循环体（要循环做的事情)
# 只要不是False或O，其他单独存在的值也会是死循环
```

#### while循环 应用

```python
i = 1	#定义一个初始值，从1开始计算，记录循环次数
s = 0	#定义一个变量保存计算结果，最开始计算结果为0，没有相加
while 1 <= 100:
    # print(s)
    s += i
    i += 1
print(s)
```

#### while循环嵌套

含义：就是while里面有while。

```python
while 条件1:
    循环体1
    while 条件2:
        循环体2
        改变变量2
    改变变量1
```

### 9 for循环

```python
基本格式:
for 临时变量 in 可迭代对象:
    循环体
# 可选代对象就是要去遍历取值的整体,现在的话只需要记符串就是可迭代对象
str = 'helloworld'
for i in str:   #i是临时变量，可以随便写，i是常规写法
    print(i)
```

#### `range()`

用来记录循环次数，相当于一个计数器

`range(start,stop,step)`

```python
for i in range(1,6):	# 从1开始，从6结束，遵循包前不包后规则  [)
    print(i)
for i in range(5):	# rangeO里面只写一个数，这个数就是循环的次数，默认从0开始
    print(i)
```

#### for循环应用

```python
j = 0	# 定义一个变量保存结果
for i in range(1,101):
    j += i
print(j)  # 相比之下，.for循环比while循环更简便一点，更常见
```

### 10 break和continue

`break` 中途退出 结束循环（结束break所在的循环）

`continue`  结束当前循环 进入下一循环

> 都是专门在循环中使用的关键字

```python
i = 1
while i <= 5:
    print(i)
    if i == 3:
        print(f'第{i}个苹果不吃了')
        i += 1
        continue
    i += 1
-----------------------
for i in  range(1,6):
    print(i)
    if i == 3:
        print(f'不吃第{i}个')
        i += 1
        # break
        continue
```

### 11 字符串编码

本质上就是二进制数据与语言文字的一一对应关系

1.2Unicode：所有字符都是2个字节，
好处：字符与数字之间转换速度更快一些坏处：占用空间大
1.3UTF-8：精准，对不同的字符用不同的长度表示优点：节省空间
缺点：字符与数字的转换速度较慢，每次都需要计算字符要用多少个字节来表示。

对于bytes，只需要知道它跟字符串类型之间的互相转换

字符串编码转换：

编码：encode() 将其他编码的字符串转换成Unicode

编码解码：decode() 将Unicode编码转换成其他编码的字符串

```python
st = '这里是六星教育'
st1 = st.encode("utf-8")
print (st1 , type(st1))
st2 = st1. decode("utf-8")
print(st2,type(st2))
```

### 12 字符串运算符

![image-20251106212853887](C:\Users\皮\AppData\Roaming\Typora\typora-user-images\image-20251106212853887.png)

`+`  字符串拼接

`*`  重复输出			注意：需要输出多少次*后面就写多少

#### 成员运算符

作用：检查字符串中是否包含了某个子字符串（即某个字符或多个字符,作为整体去找）

`in`	如果包含的话，返回True，不包含返回False

`not in`	如果不包含的话，返回True，包含返回False

### 13 字符串常见操作

**下标**

Python中下标从0开始

格式：字符串名[下标值]

```python
name = "nihao"
print(name[1])
--> i
print(name[-1])
--> o
```

**切片**

指对操作的对象截取其中一部分的操作

```python
[开始位置:结束位置:步长]
包前不包后：即从起始位置开始，到结束位置的前一位结束（不包含结束位置本身）
```

```python
st = "abcdefghij"
print(st[1:5])
--> bcde
print(st[3:])	# 下标为3之后的全部截取到
--> defghij
print(st[:7])	# 下标为7之前的全部截取到，不包含7
--> abcdefg
print(st[-1:])	# 从-1角标开始从左向右
--> j
print(st[:-5])	# abcde 从下标0到下标-5 不包含-5
--> abcde
print(st[-1:-5])	# ❌
步长：表示选取间隔，不写步长，则默认是1
步长的绝对值大小决定切取的间隔，正负号决定切取方向。正数表示从左往右取值，负数表示从右往左取值。
print(st[-1::-1])  # 下标-1开始想左间隔1步(相当于倒着打印)
--> jihgfedcba
print(st[-1:-5:-1])
--> jihg
print(st[0:7:2])
--> adg
```

___

![image-20251106220057421](C:\Users\皮\AppData\Roaming\Typora\typora-user-images\image-20251106220057421.png)

**find()**

find：检测某个子字符串是否包含在字符串中，如果在就返回这个子字符串开始位置的下标，否则就返回-1
注意：开始和结束位置下标可以省略，表示在整个字符串中查找

```python
find(子字符串，开始位置下标，结束位置下标）)
name = "bingbing"
print(name.find('i'))
--> 1
print(name.find("bing"))
--> 0
print (name.find("b",3))
--> 4
print (name.find("b",5))   #超出范围
--> -1
print (name.find("b",3,5))  #在范围3-5范围内查找
--> 4
#包前不包后
```

**index()**

检测某个子字符串是否包含在字符串中，如果在就返回这个子字符串开始位置的下标，找不到会报错

```python
index(子字符串，开始位置下标，结束位置下标)
#包前不包后
```

**count()**

返回某个子字符串在整个字符串中出现的次数，没有就返回0

```python
count(子字符串，开始位置下标，结束位置下标)
name = "bingbing"
print (name.count(nmae.count("b"))
--> 2
print (name.count(nmae.count("a"))
--> 0
print (name.count(nmae.count("b",1))
--> 1
#包前不包后
```

#### 判断

**startswith()**

是否以某个子字符串开头，是的话就返回True，不是的话就返回False，如果设置开始和结束位置则在指定范围内检查

```python
startswith(子字符串，开始位置下标，结束位置下标)
st ='sixstar'
print(st.startswith('six'))	# True
print(st.startswith('sex')) # False
print(st.startswith('s',2,6)) # False
```

**endswich()**

是否以某个子字符串结尾，是的话就返回True，不是的话就返回False，如果设置开始和结束位置则在指定范围内检查

```python
endswith(子字符串，开始位置下标，结束位置下标)
st ='sixstar'
print(st.endswith('er'))	# False
print(st.endswith('ar'))	# True
```

**isupper()**

检测字符串中所有的字母是否都为大写，是的话就返回True

```python
st ='sixstar'
print (st.isupper())
--> False
print("ST".isupper())
--> True
```

#### 修改元素

**replace()**

```python
replace(旧内容,新内容,替换次数)
注意：替换次数可以省略，默认全部替换

name = "好好学习，天天向上"
print(name.replace('天','时'))
--> 好好学习，时时向上
print(name.replzce('天','时',1))
--> 好好学习，时天向上
```

**split()**

```python
splita()：指定分隔符来切字符串

st = 'hello,python'
print(st.split('，'))
--> ['hello','python']   # 一列表的形式返回
# 如果字符串中不包含分割内容，就不进行分割，会作为一个整体
print(st.split('a'))
--> ['hello,python']
print(st.split('o'))
--> ['hell',',pyth','n']
print(st.split('o',1))
--> ['hell',',python']
```

**capitalize();lower();upper()**

```python
capitalize() 第一个字符大写，其他都小写
lower() 大写字母都转为小写
upper() 小写字母都转为大写

st ='bIngBinG'
print (st.capitalize())
--> Bingbing
print (st.lower())
--> bingbing
print (st.upper())
--> BINGBING
```

### 14 列表

定义：是处理一组有序项目的数据结构。

```python
列表名 = [元素1,元素2,元素3...]

注意：
列表的所有元素放在一对中括号门中，并使用逗号分隔开。
一个列表中的数据类型可以各不相同
--------
- 列表也可以进行切片操作
- 列表是可迭代对象，可以for循环遍历取值
```

#### 列表的相关操作

**添加元素**

`append()  extend()  insert()`

```python
append(object)	#整体添加
extend(object)	#extend分散添加，将另外一个类型中的元素逐一添加;一定要用可迭代对象
insert(index,object)	#在指定位置插入元素;定位置如果有元素，原有元素就会后移(必须指定下标)

li = ['one','two','three']
li.append('four')
print(li)
--> ['one', 'two', 'three', 'four']

li.extend('four')
print(li)
--> ['one', 'two', 'three', 'f', 'o', 'u', 'r']

li.insert(0,'four')
print(li)
--> ['four', 'one', 'two', 'three']
```

**修改元素**

```python
1 直接通过下标就可以修改
li = [1,2,3]
li[1] = 'a'
--> [1, 'a', 3]
```

**查询**

in：判断指定元素是否存在列表中，如果存在就返回True，不存在就返回False

not in：判断指定元素是否存在列表中，如果不存在就返回True，存在就返回False

```python
li = ['a','b','c','d']
print('e in li')
--> Flase
```

```python
用户输入昵称，昵称重复不能使用
# 定义一个列表，保存已经存在的昵称
name_list = ['bingbing','susu','ziyi']
while True:
    name = input('请输入你的昵称')
    if name in name_list:
        print('昵称重复，请重新输入')
    else:
        name_list.append(name)
        print(name_list)
        break
```

index：返回指定数据所在位置的下标，如果查找的数据不存在就会报错
count：统计指定数据在当前列表出现的次数
跟字符串的用法相同

**删除**

del

```python
li = ['a','b','c','d']
del li      #删除整个列表
del li[2]	#根据下标删除
print(li)
```

pop：删除指定下标的数据，python3版本默认删除最后一个元素

```python
pop(index)
--------------------------
li = ['a','b','c','d']
li.pop()
print(li)
--> ['a', 'b', 'c']
```

remove：根据元素的值进行删除

```python
remove(value)
---------------------------
li = ['a','b','c','d']
li.remove('d')
print(li)
--> ['a', 'b', 'c']
#默认删除最开始出现的指定元素(如果有两个及以上元素)
```

**排序**

`sort`    `reverse`

```python
sort：将列表按特定顺序重新排列，默认从小到大
reverse：倒序，将列表倒置（反过来）
li = [1,3,6,5,2]
li.sort()
print(li)
--> [1, 2, 3, 5, 6]

li = [1,3,6,5,2]
li.reverse()
print(li)
--> [2, 5, 6, 3, 1]
```

#### 列表推导式

```python
格式1
[表达式 for 变量 in 列表]
注意：in后面不仅可以放列表，还可以放range（）、可迭代对象
---------------------------
li = [1,2,3,4,5,6]
[print(i*5) for i in li]
--> 5
10
15
20
25
30
-------------------------
li = []
for i in range(1,6):
    li.append(i)
print(li)
--> [1, 2, 3, 4, 5]

[li.append(i) for i in range(1,6)]
--> [1, 2, 3, 4, 5]
```

```python
格式2
[表达式 for 变量 in 列表(指任何可迭代对象) if 条件]
# 把奇数放到列表里面
li = []
for i in range(1,11):
    if i%2 == 1:
        li.append(i)
print(li)
------------------------
li = []
[li.append(i) for i in range(1,11) if i%2 == 1]
print(li)     
```

#### 列表嵌套

含义：一个列表里面又有一个列表

```python
li = [1,2,3,[4,5,6]]
print(li[2])
--> 3
print(li[3][2])
--> 6
```

### 15 元组 tuple

元组格式：元组名 = （元素1，元素2，元素3...）

tua = (1,2,3）

注意：
定义元组时，如果只有一个元素，末尾要加逗号，多个元素用，隔开。不同元素也可以是不同的数据类型

``` python
tua = (1,2,3,'a','b',[1,2,3])

tub = (1)     只有一个元素的时候，末尾必须加上，  否则返回唯一值的数据类型

tua = ()       定义空元组

```

**元组与列表的区别**

- python中不允许修改元组中的数据，增删改都不支持，只支持查询
- 元组只有一个元素末尾必须加，列表不需要

元组也有下标，也是从零开始。

count()、index()、len()  跟列表的用法相同
也支持切片

**应用场景**

函数的参数和返回值

格式化输出后面的（）本质上就是一个元组

数据不可以被修改的时候，保护数据的安全

### 16 字典 dict

字典是一系列键值对组成的集合，使用花括号表示。键值之间互相关联，可以使用键来访问其关键值。

#### 字典的创建和访问

**创建**

```python
基本格式：字典名 = {键1:值1,键2:值2...}
dic = {'name':'sixStarage':18]
       
- 键值对形式保存，键和值之间用 : 隔开，每个键值对之间用 , 隔开  
- 字典值的键具备唯一性，但是值可以重复。
- 键名重复时前面的值会被后面的覆盖。
```

**查看**

```python
基本格式：1 变量名[键名]
		 2 变量名.get(键名)
- 不可以根据下标，字典中没有下标，查找元素需要键名，键名相当于下标
- 变量[] 键名不存在会报错
- .get() 键名不存在可以返回自己设置的默认值，或者返回None
-----------------------------------------------------------
dic = {'name':'bingbing','age':18}
print(dic['name'])        
print(dic.get('age'))
print(dic.get('tel','不存在'))
-->
bingbing
18
不存在
```

#### 修改、添加和删除

**修改、添加**

```python
变量名[键名] = 值
- 不存在的话会自动新建
----------------------------------------
dic = {'name':'bingbing','age':18}
dic['age'] = 20
print(dic)
dic['tel'] = 125638
print(dic)
-->
{'name': 'bingbing', 'age': 20}
{'name': 'bingbing', 'age': 20, 'tel': 125638}}
```

**删除**

```python
del                        删除整个字典
del dict[key]              删除指定的键值对，键名不存在就会报错
clear()                    清空整个字典里面的东西，但保留了这个字典
dict.pop(key,default)      删除指定的键值对并返回键对应的值，键名不存在就会报错或返回默认值
dict.popitem()             3.7之前的版本是随机删除一个键值对，3.7之后默认删除最后一对键值对
---------------------------
dic = {'name':'bingbing','age':18}
# del dic
print(dic)
del dic['age']
print(dic)
dic.clear()
print(dic.pop('age'))
print(dic.pop('age1',20))
-->
报错
{'name': 'bingbing'}
{}
18
20
```

**其他**

```python
len()       求长度
keys()      返回字典里面包含的所有键名
values()    返回字典里面包含的所有值
items()      返回字典里面包含的所有键值对，以元组的形式
-------------------------------
dic = {'name':'bingbing','age':18,'tel':123}
print(len(dic))
print(dic.keys())
for i in dic.keys():     # 只取出键名
    print(i)
print(dic.values())
for i in dic.values():     # 只取出键名
    print(i)
print(dic.item())
-->
3
dict_keys(['name', 'age', 'tel'])
name
age
tel
dict_values(['bingbing', 18, 123])
bingbing
18
123
dict_items([('name', 'bingbing'), ('age', 18), ('tel', 123)])
```

使用键值对，存储描述一个物体的相关信息

### 17 集合 set

集合格式：s1 = [1, 2, 3] 

注意：
1.集合是无序的，里面的元素是唯一的。
2.可以用于元组或者列表去重

```python
集合名 = {元素1,元素2,元素3... }
- 无序性，每次运行结果都不一样
		数字运行结果一样
  集合无序的实现方式涉及hash表（了解）
  每次运行结果都不同，hash值不同，那么在hash表中的位置也不同，这就实现了集合的无序性
  python中int整型的hash值就是它本身，在hash表中的位置不会发生改变，所以顺序也不会改变
  无序性：不能修改集合中的值
- 唯一性（自动去重）
-------------------------------
s1 = {}    #定义空字典
s1 = set()  #定义空集合
```

**添加**

```python
add()   添加的是一个整体；集合的唯一性，决定了如果需要添加的元素在原集合中已经存在，就不进行任何操作
update() 把传入的元素拆分，一个个放进集合中(可迭代对象)
---------------------------------
s2 = {1,2,3,4}
s2.add(5)
s2.add((6,7))
print(s2)
s2.update('89')
print(s2)
-->
{1, 2, 3, 4, 5, (6, 7)}
{1, 2, 3, 4, 5, (6, 7), '8', '9'}
```

**删除**

```python
remove()    选择删除的元素,必须是集合中有的元素
pop()       默认删除第一个元素
discard()   选择要删除的元素，有就会删除，没有则不会发生任何改变，即不会进行任何操作
----------------------------
s2 = {1,2,3,4}
s2.remove(3)
print(s2)
-->
{1, 2, 4}
```

**交集和并集**

```python
a ={1,2,3,4}
# b = {3, 4, 5, 6}
b = {5,6,7,8}
print(a & b)        #没有共有的部分返回空集合  set()
print(a | b)        #并集所有的都放一起，重复的不算（集合的唯一性）
```

### 18 类型转换

```python
int()   转换为一个整数，只能转换由纯数字组成的字符串，会去掉小数点及后面的数值，只保留整数部分
		如果字符串中有数字和正负（+/-）以外的字符就会报错
float() 转换为一个小数,整型转换为浮点型，会自动添加一位小数
str()   转换为字符串类型，任何类型都可以
		float转换成str会取出末尾为0的小数部分，保留一位小数
```

```python
eval()  用来执行一个字符串表达式，并返回表达式的值
		可以实现list/dict/tuple和str之间的转换
		非常强大，但是不够安全容易被恶意修改数据不建议使用
list()  将可迭代对象转换为列表
		支持转换为list的类型：str、tuple、dict、set
		字典转换成列表，会取键名作为列表的值
        基本转换成列表，会先去重，再转换
```

### 19 深浅拷贝（可变对象）

赋值

```python
赋值：会随着原对象一起变。等于完全共享资源，一个值的改变会完全被另一个值共享(列表、字典、集合等)
------------------------------------------------
li = [1,2,3,4]
li2 = li
print('li',li)
print("li2",li2)	
li.append (5)
print('新增后的li:',li)
print('新增后的li2:',li2)
-->
li [1, 2, 3, 4]
li2 [1, 2, 3, 4]
新增后的li: [1, 2, 3, 4, 5]
新增后的li2: [1, 2, 3, 4, 5]
```

**浅拷贝**

会创建新的对象，拷贝第一层的数据，嵌套层会指向原来的内存地址
外层的内层地址不同，俱是内层的内存地址相同

优点：拷贝速度快，点用空间少，拷贝效率高

```python
import copy  #导入copy模块
li = [1,2,3,[4,5,6]]
li2 = copy.copy(li)
print('li',li)
print("li2",li2)
#查看内存地址 id()
print("1i内存地址：",id(li))
print("1i2内存地址:",id(li2))
#内存地址不一样，说明不是同一个对象
li.append(8)
print('li',li)
print("li2",li2)
li[3].append(7)
print('li',li)
print("li2",li2)
print("1i内存地址：",id(li[3]))
print("1i2内存地址:",id(li2[3]))
-->
li [1, 2, 3, [4, 5, 6]]
li2 [1, 2, 3, [4, 5, 6]]
1i内存地址： 2080438706368
1i2内存地址: 2080440750976
li [1, 2, 3, [4, 5, 6], 8]
li2 [1, 2, 3, [4, 5, 6]]
li [1, 2, 3, [4, 5, 6, 7], 8]
li2 [1, 2, 3, [4, 5, 6, 7]]
1i内存地址： 2080438854592
1i2内存地址: 2080438854592
```

**深拷贝**

外层的对象和内部的元素都拷贝了一遍

```python
import copy  #导入copy模块
li = [1,2,3,[4,5,6]]
li2 = copy.deepcopy(li)
print('li',li)
print("li2",li2)
#查看内存地址 id()
print("1i内存地址：",id(li))
print("1i2内存地址:",id(li2))
#内存地址不一样，说明不是同一个对象
li.append(8)
print('li',li)
print("li2",li2)
li[3].append(7)
print('li',li)
print("li2",li2)
print("1i内存地址：",id(li[3]))
print("1i2内存地址:",id(li2[3]))
-->
li [1, 2, 3, [4, 5, 6]]
li2 [1, 2, 3, [4, 5, 6]]
1i内存地址： 1882009133248
1i2内存地址: 1882010981248
li [1, 2, 3, [4, 5, 6], 8]
li2 [1, 2, 3, [4, 5, 6]]
li [1, 2, 3, [4, 5, 6, 7], 8]
li2 [1, 2, 3, [4, 5, 6]]
1i内存地址： 1882009281472
1i2内存地址: 1882010861056
```

### 20 可变对象与不可变对象

#### 可变对象

含义：存储空间保存的数据允许被修改，这种数据就是可变类型
         变量对应的值可以修改，但是内存地址不会发生改变

常见的可变类型：
1.列表 list
2.字典 dict
3.集合 set

```python
li = [1,2,3,4]
print('原内存地址',id(li))
li.append(5)
print(li)
print('现内存地址',id(li))
dic = { 'name':'bingbing','age':18}
print (dic,id(dic))
dic['name'] = 'susu'
print (dic,id(dic))
-->
原内存地址 2365924466880
[1, 2, 3, 4, 5]
现内存地址 2365924466880
{'name': 'bingbing', 'age': 18} 2365925944960
{'name': 'susu', 'age': 18} 2365925944960
```

#### 不可变对象

含义：存储空间保存的数据不允许被修改，这种数据就是不可变类型

常见的不可变类型：
1.数值类型：int,bool,float,complex
2.字符串：str
3.元组：tuple

### 21 函数

含义：将独立的代码块组织成一个整体，使其具有特殊功能的代码集，在需要的时候再去调用即可

作用：提高代码的重用性，使整体代码看上去更加简练。

```python
定义：
def 函数名():
    函数体
    
调用：
函数名()

调用几次，函数里面的代码就会运行几次，每次调用的时候，函数都会从头开始执行

- 返回值：
函数执行结束后，最后给调用者的一个结果。
return会给函数的执行者返回值
函数中遇到return，表示此函数结束，不继续执行

1.一个返回值也没有，返回的结果是None
2.一个返回值，就把值返回给调用者
3.多个返回值，以元组的形式返回给调用者

- return和print区别
1.return表示此函数结束，print会一直执行
2.return是返回计算值，print是打印结果

- 参数
定义格式：
def 函数名(形参a,形参b):     #形参：定义函数时，小括号里面的变量
    函数体
    .. (如a = 1 b = 2)
调用格式：
函数名(实参1，实参2)		#实参：调用函数时，小括号里面的具体的值

-- 必备参数
含义：传递和定义参数的顺序及个数必须一致
格式： def func(a,b)
写了几个就必须要传几个，不可以多传，也不可以少传
 
-- 默认参数
含义：为参数提供默认值，调用函数时可不传该默认参数的值
注意：所有的位置参数必须出现在默认参数前，包括函数定义和调用
格式： def func(a=12)
设置默认值，没有传值会根据默认值来执行代码，传了值根据传入的值来执行代码

-- 可变参数
含义：传入的值的数量是可以改变的，可以传入多个，也可以不传
格式： def func(*args)  #args符合代码规范性，可以改成其他参数名
以元组形式接收

--关键字参数
格式： def func(**kwargs)
以字典形式接收
需要采用 键=值的形式 传值
作用：可以扩展函数的功能

- 函数嵌套
-- 嵌套调用
含义：在一个函数里面调用另外一个函数

-- 嵌套定义
含义：在一个函数中定义另外一个函数

----------------------------------------------------------------------
def study():
	print("晚上在学习")
def course:
	study()               #在course()函数内调用study()
    print("Python基础")
course()
----------------------------------
def study()                  #外函数
	print("晚上在学习")
	def course()             #内函数
    print("Python基础")
	course ()                 #注意：注意缩进，定义和调用是同级的，调用如果在定义里面则永远调用不到
study()
```

### 22 作用域

含义：指的是变量生效的范围，分为两种，分别是全局变量和局部变量

全局变量
函数外部定义的变量，在整个文件中都是有效的

函数内部如果要使用变量，会先从函数内部找，有的话就直接使用：没有会到函数外面去找

局部变量
函数内部定义的变量，从定义位置开始到函数定义结束位置有效
作用：在函数体内部，临时保存数据，即当函数调用完成之后，就销毁局部变量

在函数内部修改全局变量的值，可以使用global关键字，将变量声明为全局变量

```python
global 变量1,变量2...
总结：global关键字可以对全局变量进行修改，也可以在局部作用域中声明一个全局变量
```

```python
nolocal    用来声明外层的局部变量，只能在嵌套函数中使用，在外部函数先进行声明，内部函数进行nonlocal声明
总结：nonlocal只能对上一级进行修改
```

### 22 匿名函数

```python
函数名 = lamda 形参：返回值（表达式）
调用：结果=函数名（实参）
add = lamda a,b:a+b  #lambda不需要return来返回值，表达式本身结果就是返回值

- 参数形式
无参数  funa = lamda : "123"
一个    funa = lamda name:name
默认参数 funa = lamda name,age=18:(name,age)
关键字参数   fund = lambda **arwgs:arwgs
            print(fund(name = 'bingbing',age = 18))

- 结合if判断
a = 5
b = 8
#为真结果if 条件else 为假结果
# print("a比b小"）if a<b else print("a大于等于b")
comp = lambda a,b：'a比b小' if a<b else 'a大于等于b'  # a/b是形参，比较大小
print（comp（8.5））
```

### 23内置函数

```python
查看所有的内置函数
inmpot builtins
大写字母开头一般是内置常量
小写字母开头一般是内置函数

- 
abs()	返回绝对值
sum()   求和  整型不是可迭代对象，sum函数内要放可选代对象，不能字符串、字典
        运算时，只要有一个为浮点数，那么结果必定是浮点型
min()   求最小值
max()   求最大值  
        print(max(-8,5,key=abs)) 传入了求绝对值函数，则参数就会先求绝对值再取较大者
zip()   将可选代对象作为参数，将对象中对应的元素打包成一个个元组
map()   映射函数，可以对可送代对象中的每一个元素进行映射，分别去执行
        map(func,iter1)  func--自己定义的函数 iterl--要放进去的可选代对象
        简单来说就是对象中的每一个元素都会去执行这个函数
reduce() 先把对象中的两个元素取出，计算出一个值然后保存着，接下来把这个计算值跟第三个元素进行计算
		 reduce（function，sequence）  #function--函数：必须是有两个参数的函数，sequence--序列：可选代对象
---------------------
li = [1,2,3]
li2 = ['a','b']
for i in zip(li,li2):       #for循环取值
    print(i)
    print(type(i))
print(list(zip(1i,1i2)))    #转换成列表
-->
(1,'a')
<class'tuple'>
(2,'b')
<class'tuple'>
[(1,'a'),(2,'b'),(3,'c')]
-------------------------------
1i = [1,2.3]
def funa(x):
    return x * 5
mp = map(funa.li)      #注意：只要写函数名，不需要加上小括号
print(mp)

for i in map:           #for循环取值
    print(i)

print(list(mp))          #转换成列表
-->
5
10
15
-------------------------------
#需要先导包
from functools import reduce
#reduce（function，sequence）  #function--函数：必须是有两个参数的函数，sequence--序列：可选代对象
1i2 =[1.2.3.4]
def add(x,y):
    return x + y
res = reduce(add.li2)
print(res)
-->
10
```

### 24 拆包

含义：对于函数中的多个返回数据，去掉元组，列表或者字典直接获取里面数据的过程。

```python
tua =(1,2.3,4)
print(tua)
print(tua[0])     #一个一个取

a,b, c, d = tua                          #方法一  
print("a=", a,"b=", b,"c=", c,"d=", d)
-->
a= 1 b=2 c=3 d=4
要求元组内的个数与接收的变量个数相同，对象内有多少个数据就需要定义多少个变量接收
一般在获取元组值的时候使用

a, *b = tua								#方法二
print(a,b)
c,d,e = b
ptint(c,d,e)
先把单独的给它取完，其他剩下的全部都交给带*的变量

一般在函数调用时使用
def funa (a, b, *args):
    print (a, b)
	print (args, type (args) )
funa (1, 2, 3,4,5,6,7)
arg = (1, 2, 3, 4, 5, 6, 7)
funa(*arg)
-->
1 2 [3,4,5,6,7]
1 2 [3,4,5,6,7]
```

### 25 异常





















