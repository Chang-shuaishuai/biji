#python 基础

计算机内存： 存储cup要处理的数据

## python入门

### 环境的搭建

​	python解释器的作用： 翻译 python 语言为计算机语言

​	下载：https://www.python.org/downloads/release/python-390/

​	安装： 

​	![image-20201225161735795](python 入门.assets/image-20201225161735795.png)

​		

PyCharm 是一种 Python IDE（集成开发环境），带有一整套可以帮助用户在使用Python语言开发时提高效率的工具，内部集成的功能如下：

	- Project 管理
	- 智能提示
	- 语法高亮
	- 代码跳转
	- 调试代码
	- 解释代码（解释器）
	- 框架和库
	- 。。。。。

安装PyCharm

​	下载：https://www.jetbrains.com/pycharm/download/#section=windows

​	安装：

![image-20201225163703724](python 入门.assets/image-20201225163703724.png)

勾选 64-bit launcher 和  .py



####PyCharm 基本使用



![image-20201225182449647](python 入门.assets/image-20201225182449647.png)



![image-20201225165518511](python 入门.assets/image-20201225165518511.png)

新建文件并书写代码

项目根目录或根目录内部任意位置--右键 -- 【new】-- 【Python File】-- 输入文件名 -- 【OK】

>注意 : 如果是将来要上传到服务器的文件，那么文件名切记不能用中文

运行文件： 右键 run

####PyCharm 的基本设置

【file】-- 【Settings】/【Default Settings】

- Theme： 修改主题
- Name： 修改主题字体
- Size： 修改主题字号

####修改代码文字格式

	- Font: 修改字体
	- Size：修改字号
	- Line Spacing: 修改行间距

####修改解释器

进入Setting -- [Project: 项目名称] -- 【Peoject Interpreter】-- 【设置图表】-- 【add】-- 浏览到目标解释器 -- 【OK】-- 【OK】

####项目管理

打开项目

​	【File】 -- 【Open】 -- 浏览选择目标项目根目录 -- 【OK】-- 选择打开项目方式

打开项目的方式共三种，分别如下：

![image-20201225210427395](python 入门.assets/image-20201225210427395.png)

​	this window 

​		覆盖当前项目，打开新的项目

​	New window

​		在新的 PyCharm  打开项目

​	Attach 

​		在当前窗口打开多个项目

关闭项目

​	【file】-- 【Close Project】/【Close Projects in current window】

### 注释

#### 单行注释

​		快捷键 ctr+/

​		只能注释一行内容，语法如下：

```python
# 注释内容
```

> 代码后边放注释 需要在代码后边敲俩个空格 在 # 空格加注释

####多行注释

```python
"""
	第一行注释
	第二行注释
	第三行注释
"""
'''
	注释1
	注释2
	注释3
'''
```

> 单行注释通常是对一行代码的解释说明
>
> 多行注释通常是对代码块、代码对的解释说明



###  *变量

#### 变量的作用

​	程序中，数据都是临时存储在内存中，为了更快速的查找或使用这个数据，通常我们把这个数据在内存中存储之后定义一个名称，这个名称就是变量

>变量就是一个存储数据的时候当前数据所在的内存地址的名字而已

#### 定义变量

`变量名 = 值`

变量名自定义，要满足==表述符==命名规则

#### 标识符

​	标识符命名规则是Python中定义各种名字的时候的统一规范，具体如下：

		- 由数字、字母、下划线组成
		- 不能数字开头
		- 不能使用内置关键字
		- 严格区分大小写

```python
False		None	True	and		as		assert		break		class
continue	def		del		elif	else	except		finally		for
from		global	if		import	in		is			lambda		nonlocal
not			or		pass	raise	return	try			while		with
yield

```

#### 命名习惯

	- 见名知意
	- 大驼峰：既每个单词首字母都大写，例如： Myname
	- 小驼峰：第二个（含）以后的单词首字母大写，例如：myName
	- 下划线： 例如： my_name

#### 使用变量

```python
my_name = 'Tom'
print(my_name)
schoolName = '阿西吧'
print(schoolName)
```

####认识bug

![](python 入门.assets/image-20201225223144101.png)

#### Debug工具

​	Debug工具是PyCharm IDE中集成的用来调试程序的工具，在这里程序员可以查看程序的执行细节和流程或者调解bug

Debug工具

	1.  打断点
	2.  Debug调试

打断点

​	断点位置

​		目标要调试的代码块的第一行代码即可，即一个断点即可

​	打断点的方法

​		点击代码行号右边空白的位置

#### 认识数据类型	

![image-20201227124851720](python 入门.assets/image-20201227124851720.png)

```python
# int 整型
num1=1
# float 浮点型，都是小数
num2=1.1
# str 字符串 数据都要带引号
a = 'hello world'
# bool 布尔型，通常判断的时候使用
b = True
# 复杂的数据序列
# list 列表
c = [10, 20, 30]
# tuple 元组
d = (10, 20, 30)
# set 集合
e = {10, 20, 30}
# dict 字典  'name': 'TOM'  这种叫做键值对
f = {'name': 'TOM', 'age': 15}
print(type(num1))
print(type(num2))
print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
print(type(f))
```

![image-20201227125056772](python 入门.assets/image-20201227125056772.png)

### 输出

#### 格式化符号

| 格式符号 |          转换          |
| :------: | :--------------------: |
|    %s    |         字符串         |
|    %d    |   有符号的十进制整数   |
|    %f    |         浮点数         |
|    %c    |          字符          |
|    %u    |    无符号十进制整数    |
|    %o    |       八进制整数       |
|    %x    | 十六进制整数（小写ox） |
|    %X    | 十六进制整数（大写OX） |
|    %e    | 科学计数法（小写'e'）  |
|    %E    | 科学计数法（大写'E'）  |
|    %g    |      %f和%e的简写      |
|    %G    |      %f和%E的简写      |

技巧

- %06d 表示输出的整数显示位数，不足以0补全，超出当前位数则原样输出

- %.2f，表示小数点后显示的小数位数

- 格式化字符串除了%s, 还可以写为`f'{表达式}'`

- f-格式化字符串是Python3.6中新增的格式化方法，该方法更简单易读

  ```python
  age = 18
  name = 'Tom'
  weight = 75.5
  stu_id = 1
  stu_id2 = 1000
  print('今年我的年龄是%d岁' % age)
  # 位数不够补零
  print('今年我的学号是%03d岁' % stu_id)
  # 位数多了原位显示
  print('今年我的学号是%03d岁' % stu_id2)
  print('今年我的名字%s，今年%d,明年%d' % (name, age, age+1))
  print('今年我的名字%s，体重%0.2f,明年%d' % (name, weight, age+1))
  # %d %f 等和汉字连到一起最后都用字符串做展示，输出的是字符串例型，在此前提下所以都可用%s代替
  print('今年我的名字%s，今年%s,体重%s' % (name, age, weight))
  # f格式化字符串
  print(f'我的名字是{name},今年{age},明年{age+1}')
  
  ```

  ![image-20201227161452830](python 入门.assets/image-20201227161452830.png)

#### 转义字符

- `\n`：换行 
- `\t` ：制表符，一个tab键（4个空格）的距离

```python
print('hello')
print('woeld')
print('hello world')
print('hello\nworld')
print('\tabcd')


```

![image-20201227161851460](python 入门.assets/image-20201227161851460.png)

#### print结束符	

```python
print('hello', end="\n")
print('world', end="\t")
print('hello', end="...")
print('Python')
```

![image-20201227155254459](python 入门.assets/image-20201227155254459.png)

### 输入

```python
input("输入内容")
```

输入特点

+ 当程序执行到`input`，等待用户输入，输入完成之后才继续向下执行
+ 在Python中，`input`接收用户输入后，一般存储到变量，方便使用
+ 在Python中，`input`会把接收到的任意用户输入的数据都当作字符串处理

### 转换数据类型

input得到字符串类型，若想得到整型就需要转换数据类型

转换数据类型的函数

|          函数          |                         说明                         |
| :--------------------: | :--------------------------------------------------: |
|   ==int(x [ base])==   |                   将x换为一个整数                    |
|     ==float（x）==     |                 将x转换为一个浮点数                  |
| complex(real [ imag ]) |         创建一个复数，real为实部，imag为虚部         |
|       ==str(x)==       |                 将对象x转换为字符串                  |
|        repr(x)         |              将对象x转换为表达式字符串               |
|     ==eval(str)==      | 用来计算在字符串中的有效Python表达式，并返回一个对象 |
|      ==tuple(s)==      |                将序列s转换为一个元组                 |
|     ==list（s）==      |                将序列s转换为一个列表                 |
|         chr(x)         |           将一个整数转换为一个Unicode字符            |
|         ord(x)         |           将一个字符转换为它的ASCll整数值            |
|         hex(x)         |          将一个整数转换为一个十六进制字符串          |
|        otc（x）        |           将一个整数转换为一个八进制字符串           |
|         bin(x)         |           将一个整数转换为一个二进制字符串           |

```python
# 将数据转换为浮点型
num1 = 1
str1 = '10'
print(type(float(num1)))
print(float(num1))
print(float(str1))
# 将数据转换为字符串类型
print(type(str(num1)))
print(str(num1))
# 将一个序列转换为元组
list1 = [10, 20, 30]
print(type(tuple(list1)))
print(tuple(list1))
# 将一个序列转换为列表
t1 = (100, 200, 300)
print(type(list(t1)))
print(list(t1))
# 计算在字符串中的有效Python表达式，并返回一个对象 所人话就是根据字符串应该对应的类型转为这种类型
str2 = '1'   # 转整型
str3 = '1.1'  # 转浮点型
str4 = '(1000, 2000, 3000)'  # 转元组
str5 = '[1000, 2000, 3000]'  # 转列表
print('\n')
print(type(eval(str2)))
print(type(eval(str3)))
print(type(eval(str4)))
print(type(eval(str5)))
```



![image-20201227170158520](python 入门.assets/image-20201227170158520.png)



### PyCharm 交互式开发

![image-20201227170809700](python 入门.assets/image-20201227170809700.png)

​	可以实现的效果就是，可以直接书写代码，不用 print 也可直接输出，可快速的展示结果给程序员

​	可以交互式测试，但是不保存代码

### 运算符

#### 运算符的分类

+ 算数运算符
+ 赋值运算符
+ 复合运算符

## 流程控制

### 条件语句

### 循环



## 数据序列

### 字符串

### 列表

### 字典

### 元组



## 函数

### 参数

### 返回值

### 递归

###lambda 表达式



## 文件操作

### 打开和关闭

### 读取和写入



## 面向对象

### 类和对象

### 继承

###面向对象高级

##模块、包、异常

## 综合实战



