---
title: python基础
date: 2017-12-13 19:47:07
tags:
  - python
  - 语言
categories:
  - 就会这么点语言
---
{% asset_img 1.jpg PYTHON %}
<!-- more -->
# 安装
## 在GNU/Linux下安装
```
sudo apt-get update && apt-get install python3

```
## 编辑器
<li> 教育版的PyCharm
<li> Vim + jedi-vim

# 基础
## 注释
  **注释**是任何存在于**#**号右侧的文字，主要作用是写给读者看的笔记
```
print('hello world') # print 函数

```
## 字面常量
  一个字面常量（Literal Constants）的例子是诸如5、1.23这样的数字，或者是如`这是一串文本` 或 `This is a string` 这样的文本。

## 数字
<li> 整数 Integers
<li> 浮点数 Floats

## 字符串
  一串字符串（String）是字符（Characters）的序列（Sequence）。
  字符串是不可变的。

## 引号
<li> 单引号

  `'Quote me on this'`

<li> 双引号

  `"What's your name?"`

<li> 三引号

  用来指定多行字符串，可以在三引号之间自由换行。

## 格式化方法

  使用**format()**方法从其他变量构建字符串。
  如，str_format.py:

  ```
    age = 20
    name = 'Swaroop'

    print('{0} was {1} years old when he wrote this book'.format(name,age))

  ```

## 转义序列
<li> 换行符`\n`
<li> 制表符`\t`
<li> 单引号`\'`

  `What\'s your name?`
<li> 原始字符串

  未经特殊处理的字符串，比如转义序列，要在字符串前加**r**或**R**, 例如
    `r"Newlines are indicated by \n"`
  > 使用正则表达式时应全程使用**原始字符串**

## 变量 Veriables
> 变量的值可以变化
## 对象 Object
> Python是**强面向对象**的，因为所有的一切都是对象，包括<*数字、字符串与函数*.

## 逻辑行与物理行
<li> Physical Line
  > 编写程序是所看到的内容
<li> Logical Line
  > Python编辑器所看到的单个语句

  ```
  # 一个物理行，两个逻辑行
  i = 5; print(i);

  # 两个物理行，两个逻辑行
  i = 5;
  print(i)
  ```
<li> 显式行连接
如果有一行非常长的代码，可以用反斜杠将其拆分成多个物理行
  ```
  s = 'This is a string, \
  This continues the string.'
  ```
<li> 隐式行连接
逻辑行以括号开始。

## 缩进
**空白区**在Python中十分重要。逻辑行的开头留下空白区（空格或者制表符）用以确定行的缩进级别，并且确定语句分组。
具有相同缩进的语句被称为**块(block)**
---
# 运算符与表达式
## 运算符
<li> `+`
<li> `-`
<li> `<li>`
<li> `**` 乘方
<li> `/`
<li> `//` 整除
  > x 除以 y 并对结果向下取整

<li> `%`
<li> `<<` 左移
  > 二进制

<li> `>>` 右移
  > 二进制

<li> `&` 按位与
<li> `|` 按位或
<li> `^` 按位异或
<li> `~` 按位取反
<li> `<`, `<=`
<li> `>`, `>=`
<li> `==`, `!=`
<li> `not`, `and`, `or`
## 数值运算与赋值的快捷方式
<li> `变量 = 变量 运算 表达式` --> `变量 运算 = 表达式`
<li> 求值顺序
  > 最好使用**圆括号**进行分组

  <li> `ambda`: Lambda 表达式
  <li> `if - else`: 条件表达式
  <li> `or`
  <li> `and`
  <li> `not x`
  <li> `in`, `not in`, `is`, `is not`, `<`, `<=`, `>`,` >=`, `!=`,` ==`
  <li> `|`
  <li> `^`
  <li> `&`
  <li> `<<`, `>>`
  <li> +, -
  <li> `<li>`, `/`, `//`
  <li> `+x`,` -x`, `~x` :正、负、按位取反
  <li> `**`
  <li> `x[index]`, `x[index:index]`, `x(arguments...)`, `x.attribute` :下标、切片、调用、属性引用
  <li> `(expressiongs...)`, `[expressions...]`, `{key:value...}`, `{expressions...}` : 显示绑定或数组、显示列表、显示字典、显示设置

  > 上述优先级从下往上越来越高
---
# 控制流
Python中有三种控制流语句-`if`,`for` 和 `while`。
## **if** 语句
*if* 语句用以检查条件：如果条件为真（True）

  ```
  number = 23;
  guess = int(input('Enter an integer : '))

  if guess == number:
      print('Congratulations, you guessed it.')
      print('(but you do not win any prizes!)')
  elif guess < number:
      print('No, it is a little higher than that')
  else:
      print('No, it is a little lower than that')

  print('Done')
  ```

## **while** 语句
*while* 语句当条件为真时重复执行某块语句

```
number = 23
running = True

while running:
    guess = int(input('Enter an integer : '))
    if guess == number:
        print('Congratulations, you guess it.')
        running = False
    elif guess <=number:
        print('No, it is a little higher than that.')
    else:
        print('No, it is a little lower than that.')
else:
    print('The while loop is over.')

print('Done')

```

## **for** 语句
<li>for...in<li> 语句会在一系列对象上进行迭代（Iterates）。

```
for i in range(2, 5):
    print(i)
else:
    print('The for loop is over')

```
  > `range()` 函数生成数字序列

---
# 函数
**函数** 是指可重复使用的程序片段。通过关键词***def***来定义。

<li> 案例一 无参函数

  ```
    def say_hello():
        print('hello world')

    say_hello()
    say_hello()
  ```
<li> 案例二 带参函数

  ```
    def print_max(a, b):
      if a > b:
          print(a, 'is maximum')
      elif a == b:
          print(a, 'is equal to', b)
      else:
          print(b, 'is maximum')

    print_max(3, 4)

    x = 5
    y = 7
    print_max(x, y)
  ```
<li> 案例三 局部变量

只在声明的函数内起作用
  ```
  x = 50

  def func(x):
      print('x is', x)
      x = 2 # 局部变量
      print('Changed local x to', x)

  func(x)
  print('x is still', x)                   
  ```

<li> global 语句

通过关键字**global**，确定变量是在最外面的代码块中定义的
  ```
  x = 50

  def func():
      global x # global关键字

      print('x is',x)
      x = 2
      print('Changed global x to',x)

  func() # 此处没有传递变量
  print('Value of x is', x)

  ```

<li> 默认参数值

当用户不想提供此参数值时。

  ```
  def say(message, times=1):
    print(message * times)

  say('Hello')
  say('World', 5)         
  ```
<li> 关键字参数 Keyword arguments

只希望对函数的某些参数进行指定。
> 优点
>> <li> 不用考虑参数顺序
>> <li> 只对我们希望赋予的参数赋值，只要其他的参数具有默认参数值

  ```
  def func(a, b=5, c=10):
    print('a is', a, 'and b is', b, 'and c is', c)

  func(3, 7) # 赋值a=3,b=7,c是默认参数值
  func(25, c=24) # 赋值a=25,c=24,b是默认参数值
  func(c=50,a=100) # 赋值a=100,c=50,b是默认参数值，并且打乱参数顺序           
  ```
<li> 可变参数

定义的函数里面有任意数量的变量，通过**\*** 来实现

  ```
  def total(a=5, *numbers, **phonebook):
    print('a', a)

    # 遍历元组中所有项目
    for single_item in numbers:
        print('single_item', single_item)

    # 遍历字典中所有项目
    for first_part, second_part in phonebook.items():
        print(first_part, second_part)

  print(total(10,1,2,3,Jack=1123,John=2231,Inge=1560))

  ```
  > 一颗**\***表示元组(Tuple)
  > 两颗**\*\***表示字典(Dictionary)

<li> return 语句

从函数中返回


<li> **DocStrings**

**文档字符串**，更好的记录程序，并加易于理解

  ```
  def print_max(x, y):
    '''Prints the maximum of two numbers.

    The two values must be integers.'''

    x = int(x)
    y = int(y)

    if x > y:
        print(x, 'is maximum')
    else:
        print(y, 'is maximum')

  print_max(3, 5)

  print(print_max.__doc__)

  ```

  ---

# 模块
复用函数。
一个模块可以被其他程序导入并运用其功能。

  ```
  import sys

  print('The command line arguments are:')
  for i in sys.argv:
      print(i)

  print('\n\nThe PYTHONPATH is', sys.path, '\n')
  ```
  > `import sys`导入了sys模块

## 按字节码编译的**.pyc**文件
创建按字节码编译的(Byte-Compiled)文件，以.pyc作为扩展名，是Python的中间形式。
<li> **from...import**语句

使用`from...import`导入模块，可以避免每次调用模块里函数都要输入模块名，`sys.argva`，但是最好使用`import`导入模块，可以避免名称冲突

<li> 模块的 `__name__`

用来确定模块是独立运行的还是被导入来运行的。
  ```
  if __name__ == '__main__':
      print('This program is being run by itself')
  else:
      print('I am being imported from another module')
  ```

## 编写自己的模块
每个Python程序同时也是一个模块。
<li> 建立模块`mymodule.py`

  ```
  def say_hi():
      print('Hi, this is mymodule speaking.')

  __version__ = '0.1'

  ```

<li> 引用模块`mymodule.py`，创建`mymodule_demo.py`

  ```
  import mymodule

  mymodule.say_hi()
  print('Version', mymodule.__version__)        
  ```

  > 模块要与程序在同一目录下，或者放在sys.path所列出的其中一个目录下

## 包
包（package）把模块组织起来。
包是指一个包含模块与一个特殊的**\_\_init\_\_.py**文件夹。
包的结构如图所示，
{% asset_img packagestruct.jpg 包结构 %}
  > `world`为包名，其他文件夹、子文件夹为子包或模块

---

# 数据结构
Python有四中内置的数据结构
  > <li> ***List***
  > <li> ***Tuple***
  > <li> ***Dictionary***
  > <li> ***Set***

## 列表

**列表** 是一种用于保存一系列有序项目的集合。用`[...]`括起来，可以对列表进行***添加、移除或搜索***操作。

<li> 案例

`ds_using_list.py`

``` ds_using_list.py
# This is my shopping list
shoplist = ['apple', 'mango', 'carrot', 'banana']

print('I have', len(shoplist), 'items to purchase')

print('These items are:', end=' ')
for item in shoplist:
    print(item, end=' ')

print('\nI also have to buy rice.')
shoplist.append('rice')
print('My shopping list is now', shoplist)

print('I will sort my list now')
shoplist.sort()
print('Sorted shopping list is', shoplist)

print('The first item I will buy is', shoplist[0])
olditem = shoplist[0]
del shoplist[0]
print('I bought the', olditem)
print('My shopping list is now', shoplist)
```

> 变量`shoplist`是一张购物清单。在`shoplist`中存储了一些字符串，也可以向其中添加任何类型的对象，包括数字，甚至其他列表。

## 元组
**元组** 将多个对象保存到一起，可以近似地看做列表，但是功能很少。元组类似于字符串，是不可变的。
**元组** 是通过特别指定项目来定义的，形式`x = (...,...,...,)`，括号非必选，也可以`a = ...,...,...`。
**元组** 通常用来保证某一语句或某一用户定义的函数可以安全地采用一组数值。

<li> 案例

`ds_using_tuple.py`

```
zoo = ('python', 'elephant', 'penguin')
print('Number of animals in the zoo is', len(zoo))

new_zoo = 'monkey', 'camel', zoo
print('Number of cages in the new zoo is', len(new_zoo))
print('All animal in new zoo are', new_zoo)
print('Animals brought from old zoo are', new_zoo[2])
print('Last animal brought from old zoo is', new_zoo[2][2])
print('Number of animals in the new zoo is', len(new_zoo)-1+len(new_zoo[2]))
```
输出:

```
Number of animals in the zoo is 3
Number of cages in the new zoo is 3
All animal in new zoo are ('monkey', 'camel', ('python', 'elephant', 'penguin'))
Animals brought from old zoo are ('python', 'elephant', 'penguin')
Last animal brought from old zoo is penguin
Number of animals in the new zoo is 5
```
> <li> 元组也是一个序列。
> <li> 空元组由一对圆括号构成，就像`myempty = ()`。
> <li> 如果只有一个项目的元组，必须在项目后面加上逗号`,`，`singleton = (2, )`。

## 字典
**字典**就是键值对，就像地址簿，知道姓名就可以查找到地址，但是键值必须唯一。形式，`d = {key : value, key2 : value2}`。
**键值**是不可变的对象。
**字典**中的键值不会进行排序，只能在使用前进行排序。

<li> 案例

`ds_using_dict.py`

```
ab = {
    'Swaroop': 'swaroop@swaroopch.com',
    'Larry': 'larry@wall.org',
    'Matsumoto': 'matz@ruby-lang.org',
    'Spammer': 'spammer@hotmail.com'
}

print("Swaroop's address is", ab['Swaroop'])

# 删除一对键值-值配对
del ab['Spammer']

print('\nThere are {} contacts in the address-bok\n'.format(len(ab)))

for name, address in ab.items():
    print('Contact {} at {}'.format(name, address))

# 添加一对键值-值配对
ab['Guido'] = 'guido@python.org'

if 'Guido' in ab:
  print("\nGuido's address is", ab['Guido'])
```

输出

```
Swaroop's address is swaroop@swaroopch.com

There are 3 contacts in the address-bok

Contact Matsumoto at matz@ruby-lang.org
Contact Larry at larry@wall.org
Contact Swaroop at swaroop@swaroopch.com
```

## 序列
**列表、元组和字符串**都是序列(Sequence)的某种表现形式。
**序列**的主要功能：
  <li> 资格测试 Membership Test
  <li> 索引操作 Indexing Operations

**切片**: Slicing运算符，可以获得序列中的某一段。
**案例**
`ds_seq.py`

```
shoplist = ['apple', 'mango', 'carrot', 'banana']
name = 'swaroop'

print('Item 0 is',shoplist[0])
print('Item -1 is', shoplist[-1])

print('Character 0 is', name[0])

print('Item 1 to 3 is', shoplist[1:3])
print('Item 1 to -1 is', shoplist[1:-1])
print('Item start to end is', shoplist[:])
```
***输出***

```
Item 0 is apple
Item -1 is banana
Character 0 is s
Item 1 to 3 is ['mango', 'carrot']
Item 1 to -1 is ['mango', 'carrot']
Item start to end is ['apple', 'mango', 'carrot', 'banana']
```

> <li> 获取序列中的一个对象，可以用单个数字来，比如 `shoplist[0]`，也可以使用负数`shoplsit[-1]`，**-1**表示最右端的对象。
> <li> 获取连续的片断，开始和结束位置用`：`隔开，比如`shoplist[1:3]`，**1**表示开始位置，**3**表示结束时的位置，即获取的子序列为`1,2`。

## 集合
**集合 Set** 是简单对象的无序集合。
表示形式，`bri = set(['brazil', 'russia', 'india'])`。
基本操作参见数学里的集合操作。

## 引用
当创建一个对象并将其分配给某个变量时，变量只会**查阅 Refer**某个对象，也就是说变量名只是指向计算机内存中存储了相应对象的那一部分。又称为**名称绑定 Binding**给那一个对象。

**案例**
`ds_reference.py`
```
print('Simple Assignment')
shoplist = ['apple', 'mango', 'carrot', 'banana']
# mylist 只是指向同一对象的另一种名称
mylist = shoplist

del shoplist[0]

print('shoplist is', shoplist)
print('mylist is', mylist)

print('Copy by making a full slice')

mylist = shoplist[:]

del mylist[0]

print('shoplist is', shoplist)
print('mylist is', mylist)
```

**输出**

```
Simple Assignment
shoplist is ['mango', 'carrot', 'banana']
mylist is ['mango', 'carrot', 'banana']
Copy by making a full slice
shoplist is ['mango', 'carrot', 'banana']
mylist is ['carrot', 'banana']
```
> 如果想要创建一份诸如序列等复杂对象的副本，必须使用切片操作来制作副本。如果仅仅通过复制变量名，那么他们为同一引用。

# 解决问题
如何用***Python***解决实际问题。
## Target
> 一款可以备份所有重要文件的程序

## Ayalysis

> <li> 需要备份的文件与目录应在一份列表中予以指定
> <li> 备份必须存储在一个主备份目录中
> <li> 备份文件将打包压缩成zip文件
> <li> zip压缩文件的文件名由当前日期和时间构成

## Implementation V1

**代码**
`backup_v1.py`

```
# 指定在同一个列表中
# 例如在Windows下：
# source = ['"C:\\My Documents"', 'C:\\Code']
# 又如在Mac OS x 与Linux下：
source = ['/home/starsea/workspace/python3/basic']
# 如果字符串中包含空格，要先用双引号括起来

# 2. 备份文件必须存储在主备份目录中
# 例如在Windows下：
# target_dir = 'E:\\Backup'
# 又如在Mac OS X 与Linux下：
target_dir = '/home/starsea/workspace/python3/basic/backup'

# 3. 备份文件将打包文件压缩成zip文件
# 4. zip文件名由当前日期与时间构成
target = target_dir + os.sep + time.strftime('%Y%m%d%H%M%S') + '.zip'

# 如果目录不存在则创建
if not os.path.exists(target_dir):
    os.mkdir(target_dir)

# 5.使用zip命令将文件打包成zip格式
zip_command = 'zip -r {0} {1}'.format(target, ' '.join(source))
# 运行备份
print('Zip command is:')
print(zip_command)
print('Running:')
if os.system(zip_command) == 0:
    print('Successful backup to', target)
else:
    print('Backup FAILED')
```
## Implementation V2

实现时间作为文件名，存储在以当前日期为名字的文件夹中

`backup_v2.py`

```
import os
import time

source = ['./basic/']

target_dir = '/home/starsea/backup'

if not os.path.exists(target_dir):
    os.mkdir(target_dir)

today = target_dir + os.sep + time.strftime('%Y%m%d')

now = time.strftime('%H%M%S')

target = today + os.sep + now + '.zip'

if not os.path.exists(today):
    os.mkdir(today)
    print('Successfully created directory', today)

zip_command = 'zip -r {0} {1}'.format(target, ' '.join(source))

print('Zip command is:')
print(zip_command)
if os.system(zip_command) == 0:
    print('Successful backup to', target)
else:
    print('Backup FAILED')
```

## Implementation V3

实现添加注释到文件名

`backup_v3.py`

```
import os
import time

source = ['./basic']

target_dir = '/home/starsea/backup'

if not os.path.exists(target_dir):
    os.mkdir(target_dir)

today = target_dir + os.sep + time.strftime('%Y%m%d')

now = time.strftime('%H%M%S')

comment = input('Enter a comment -->')

if len(comment) == 0:
    target = today + os.sep + now + '.zip'
else:
    target = today + os.sep + now + '_' + comment.replace(' ', '_') + '.zip'

if not os.path.exists(today):
    os.mkdir(today)
    print('Successful created directory', today)

zip_command = "zip -r {0} {1}".format(target, ' '.join(source))

print('Zip command is:')
print(zip_command)
print('Running:')
if not os.system(zip_command) == 0:
    print('Successful backup to', target)
else:
    print('Backup FAILED')

```

## Implementation V4

更换`os.system()`为`zipfile.ZipFile()`

`backup_v4.py`

```
import os
import time
import zipfile

source = ['./basic']

target_dir = '/home/starsea/backup'

if not os.path.exists(target_dir):
    os.mkdir(target_dir)

today = target_dir + os.sep + time.strftime('%Y%m%d')

now = time.strftime('%H%M%S')

comment = input('Enter a comment -->')

if len(comment) == 0:
    target = today + os.sep + now + '.zip'
else:
    target = today + os.sep + now + '_' + comment.replace(' ', '_') + '.zip'

if not os.path.exists(today):
    os.mkdir(today)
    print('Successful created directory', today)


print('Running:')

with zipfile.ZipFile(target, mode='w') as zipf:
    for filedir in source:
        for files in os.listdir(filedir):
            filepath = filedir + os.sep + files
            print('add file {0} to {1}'.format(filepath, target))
            zipf.write(filepath)
```
---
# 面向对象编程
**类**与**对象**是面向对象编程的两个主要方面。一个**类 Class**能够创建一种新的**类型 Type**，其中**对象 Object**就是类的**实例 Instance**。
> 类包括：
  > <li> 字段 Field
  > <li> 方法 Method
> 统称为类的<b>属性 Attribute<b>。

**类**通过`class`关键字创建。

## self
类中的方法都有一个必须的参数`self`，不必为其赋值，Python会为其提供。`self`引用的是对象本身。

## 类
具体例子
`oop_method.py`

```
class person:
    def say_hi(self):
        print('Hello, how are you?')

p = person()
p.say_hi()
```
### `__init__`方法
`__init`有两个下划线`_`。
`__init__`方法会在类的对象被实例化时立即运行，类似于JAVA的构造函数。
案例 `oop_init.py`

```
class Person:
    def __init__(self, name):
        self.name = name

    def say_hi(self):
        print('Hello, my name is', self.name)

p = Person('Swarrop')
p.say_hi()
```
### 类变量与对象变量

<li> **类变量**是共享的，可以被所有属于该类的实例访问。
<li> **对象变量**由类的每一个独立的对象或实例所拥有。

案例 `oop_objvar.py`

```
class Robot:
    # Class variable
    population = 0

    def __init__(self, name):
        self.name = name
        print("(Initializing {})".format(self.name))

        Robot.population += 1

    def die(self):
        print('{} is being destroyed!'.format(self.name))
        Robot.population -= 1
        if Robot.population == 0:
            print('{} was the last one.'.format(self.name))
        else:
            print('There are still {:d} robots working.'.format(Robot.population))

    def say_hi(self):
        print('Greeting, my masters call me {}.'.format(self.name))

    @classmethod
    def how_many(cls):
        print('We have {:d} robots.'.format(cls.population))

droid1 = Robot('R2-D2')
droid1.say_hi()
Robot.how_many()

droid2 = Robot('C-3P0')
droid2.say_hi()
Robot.how_many()

print('\nRobots can do some work here.\n')

print("Robots have finised their work. So let's destroy them.")
droid1.die()
droid2.die()

Robot.how_many()
```
> `population`为类变量，可以通过类名访问，`Robot.population`
> 声明一个属于类的方法，使用**装饰器 Decorator**对方法进行标记。

## 继承
面向对象一大优点是通过**继承 Inheritance**实现代码的**重用 Reuse**。

案例 `oop_subclass.py`

```
class SchoolMember:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        print('(Initialized SchoolMember: {})'.format(self.name))

    def tell(self):
        print('Name: {0} Age: {1}'.format(self.name, self.age), end = ' ')

class Teacher(SchoolMember):
    def __init__(self, name, age, salary):
        SchoolMember.__init__(self, name, age)
        self.salary = salary
        print('(Initialized Teacher: {}'.format(self.name))

    def tell(self):
        SchoolMember.tell(self)
        print('Salary: {:d}'.format(self.salary))

class Student(SchoolMember):
    def __init__(self, name, age, marks):
        SchoolMember.__init__(self, name, age)
        self.marks = marks
        print('(Intialized Student {})'.format(self.name))

    def tell(self):
        SchoolMember.tell(self)
        print('Marks: {:d}'.format(self.marks))

t = Teacher('Mrs. Shrividya', 40, 30000)
s = Student('Swaroop', 25, 75)

print()

members = [t, s]

for member in members:
    member.tell()
```
> <li> `SchoolMember`被称为**基类 Base Class**或者**超类 Superclass**
> <li> `Teacher`和`Student`被称为**派生类 Derived Classes**或是**子类 Subclass**。

> **多重继承 Multiple Inheritance**，同时继承多个类

---

# 输入与输出
主要的需求是获取用户的输入与输出和处理文件。

## 用户输入内容
案例 `io_input.py`

```
def reverse(text):
    return text[::-1]

def is_palindrome(text):
    return text == reverse(text)

something = input('Enter text: ')

if is_palindrome(something):
    print('Yes, it is a palindrome')
else:
    print('No, it is not a palindrome')
```

> `input()`函数接受一个字符串作为参数，**回车键**表示结束输入。

## 文件
通过创建一个属于`file`类的对象，可以通过方法`read(),readline(),write()`进行读写操作。最后要用`close()`方法关闭打开的文件。

案例 `io_using_file.py`

```
poem = '''\
Programming is fun
When the work is done
if you wanna make your work also fun:
    use Python!
'''

f = open('poem.txt', 'w')

f.write(poem)

f.close()

f = open('poem.txt')
while True:
    line = f.readline()
    if len(line) == 0:
        break
    print(line, end='')

f.close()
```
> 每次使用完文件务必用`close()`方法关闭。

> `opencv(name, mode)`，mode可以有几种模式：
  > <li> `r`，只读模式，默认模式
  > <li> `w`, 写入模式
  > <li> `a`, 追加模式
  > <li> `rt, wt, at`， 文本模式
  > <li> `rb, wb, ab`， 二进制模式

## Pickle
这是Python的一个标准模块，可以将对象**持久化 Persistention**。

案例 `io_pickle.py `

```
import pickle

shoplistfile = 'shoplist.data'
shoplist = ['apple', 'mango', 'carrot']

f = open(shoplistfile, 'wb')

pickle.dump(shoplist, f)

f.close()

del shoplist

f = open(shoplistfile, 'rb')

storedlist = pickle.load(f)

print(storedlist)
```
> 要用二进制的模式打开。

## Unicode
想要处理其它非英语字符，需要Unicode编码

案例 `io_using_utf-8.py`
```
# encoding=utf-8
import io

f = io.open('abc.txt', 'wt', encoding='utf-8')
f.write(u'Imaging non-English languange here')
f.close()

text = io.open('abc.txt', encoding='utf-8').read()
print(text)
```
> 需要在文件开头加上`# encoding=utf-8`。

# 异常
当程序发生错误时，会**抛出 Raise**异常。

案例 `exceptions_handle.py`

```
try:
    text = input('Enter something -->')
except EOFError:
    print('Why did you do an EOF on me?')
except KeyboardInterrupt:
    print('You cancelled the operation.')
else:
    print('You entered{}'.format(text))
```
## 手动抛出异常
通过`raise`语句抛出异常，具体方法是提供错误名或异常名以及要抛出异常的对象。
案例 `exceptions_raise.py`
```
class ShortInputException(Exception):
    def __init__(self, length, atleast):
        Exception.__init__(self)
        self.length = length
        self.atleast = atleast

try:
    text = input('Enter something -->')
    if len(text) < 3:
        raise ShortInputException(len(text), 3)
except EOFError:
    print('Why did you do an EOF on me?')
except ShortInputException as ex:
    print(('ShortInputException: The input was ' + '{0} long, expected at least {1}').format(ex.length, ex.atleast))

else:
    print('No exception was raised')
```
## Try...Finally
通常在`finally`里把打开的文件关闭。

案例 `exceptions_finally.py`
```
import sys
import time

f = None
try:
    f = open('poem.txt')
    while True:
        line = f.readline()
        if len(line) == 0:
            break
        print(line, end='')
        sys.stdout.flush()
        print('Press ctrl+c now')
        time.sleep(2)
except IOError:
    print('Could not find file poem.txt')
except KeyboardInterrupt:
    print('!! You cancelled the reading from the file.')
finally:
    if f:
        f.close()
    print('Cleaning up: Closed the file')
```
> `print()`方法后使用`sys.stout.flush()`可以立即打印到屏幕。

## with
使用`with`语句打开文件，不用再在`finally`里面对文件进行关闭。
案例 `exceptions_using_with.py`
```
with open('poem.txt') as f:
    for line in f:
        print(line, end='')
```
