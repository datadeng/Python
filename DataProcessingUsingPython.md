#走近Python
##python简介

##第一个python程序
+ 经典Hello world：两种方式运行程序（source,file）
+ python输出：print语句
	+ print变量
	+ print字符串
+ python输入：raw_input(),返回的类型是字符型
+ pyhton风格：
	+ 风格二：使用续行符号：'\'
		+ 无需换行符直接换行情况：小括号、中括号、花括号内部都可以多行书写
		+ 三行引号包含下的字符串也可以跨行书写
	+ 风格三：一行多语句
	+ 风格四：缩进
##解释器
+ Python既可以在Shell中运行执行，也可以存储成以.py为扩展名的文本文件使用Python解释器去执行

##使用文本编辑器（Sublime Text、Notepad++）
Python的交互模式和直接运行.py文件的区别

+ 直接输入python进入交互模式，相当于启动了Python解释器，但是等待你一行一行地输入源代码，每输入一行就执行一行。

+ 直接运行.py文件相当于启动了Python解释器，然后一次性把.py文件的源代码给执行了，你是没有机会输入源代码的。

+ 用Python开发程序，完全可以一边在文本编辑器里写代码，一边开一个交互式命令窗口，在写代码的过程中，把部分代码粘到命令行去验证，事半功倍！

##输入和输出
+ 任何计算机程序都是为了执行一个特定的任务，有了输入，用户才能告诉计算机程序所需的信息，有了输出，程序运行后才能告诉用户任务的结果。

+ 输入是Input，输出是Output，因此，我们把输入输出统称为Input/Output，或者简写为IO。

+ raw_input和print是在命令行下面最基本的输入和输出，但是，用户也可以通过其他更高级的图形界面完成输入和输出，比如，在网页上的一个文本框输入自己的名字，点击“确定”后在网页上看到输出信息。

+ raw_input和input函数均能接收字符串 ，但raw_input()直接读取控制台的输入（任何类型的输入它都可以接收。而对于input()，它希望能够读取一个合法的python表达式，即你输入字符串的时候必须使用引号将它括起来，否则它会引发一个SyntaxError；raw_input()将所有输入作为字符串看待，返回字符串类型。而 input() 在对待纯数字输入时具有自己的特性，它返回所输入的数字的类型（int,float）；同时input()可接受合法的python表达式,举例：input(1+3) 会返回int型的 4

##运算
+ 分片：分片的操作需要提供两个索引作为边界，第一个索引的元素是包含在分片内的，而第二个不包含的分片内

##函数
+ 内置函数：str(),type()
+ 
##模块
+ 非内建函数使用：导入相应模块
+ 一个完整的python文件就是一个模块
+ 导入模块：import 模块名；导入模块中函数：from 模块名 import 函数

##包
+ 一个有层次文件目录结构
+ 定义一个模块和子包组成的Python应用程序开发环境 
+ import AAAA.CCC.c1;AAA.CCC.c1.func1(123)(from AAA.CCC.c1 import func1)

##库
+ 库是一组具有相关功能的模块集合

#python面面观
##条件
+ if语句：if 表达式：代码块
+ else语句：if 表达式：代码块  else：代码块
+ elif语句：if 表达式：代码块  elif 表达式：代码块
+ 条件嵌套：同等缩进为同一条件结构

##range和xrange
###range()
+ range(start,end,step=1)
+ range(start,end)
+ range(end)
+ start(起始值，包含)，end(终止值，不包含)
+ 生成真实的列表

###xrange()
+ 返回生成器，用多少生成多少，节约空间

##循环
+ while循环：while 条件表达式：代码块
+ for循环：for 一个变量 in 列表集合：代码块；字符串就是一个iterable_object,range()返回列表集合

##循环中加入break、continue、else
+ break语句：终止当前循环，执行循环之后的语句
+ continue语句：跳出当前循环，继续执行程序

##自定义函数
+ def 函数名（【参数】）：”文档字符串“，代码块
+ 默认参数：默认参数的值可以更改；默认参数放在参数列表最后
+ 关键字参数：
+ 传递函数
+ lambda函数：匿名函数
+ in函数：用于字符串、列表中是否包含

##递归
+ 递归必须要有边界条件，即停止条件
+ 递归代码更加简洁

##变量作用域
+ 全局变量：程序主题部分
+ 局部变量：函数内部
+ 同名变量：内层屏蔽外层
+ global语句：强调全局变量

#数据获取
##本地数据获取
+ 打开文件：f=open(r'文件路径'，'w'),使用r关闭转义机制
+ 读文件，写文件
+ 关闭文件
+ 文件打开
file_obj=open(filename,mode='r',buffering=-1)
	mode可选参数，默认值为r
	buffering也为可选参数，默认为-1，
+ open函数
+ 文件相关函数：对象.方法（参数）

##网络数据获取

##序列
+ 值比较、对象身份比较（in,not in）、逻辑运算

##字符串
+ 字符串不同表示方法
+ 格式运算符
+ 转义字符（\"表示双引号，\t横向制表符）

##列表
+ 可扩展的容器对象，包含不同的类型对象
+ 列表解析：[exp for expr1 in 序列1
+               for expr2 in 序列2
+               if 条件]

##元祖
+ 列表元素可变、元祖元素不可变
+ sorted()不改变列表、元祖，只是产生复本；sort（）改变列表，不改变元祖
+ 元祖用处：作为函数形式参数，作为函数返回的常见类型

#强大的数据结构
##为什么使用数据字典
+ 字典定义：一种映射关系：键值对：key-value
+ 创建字典：直接、利用dict函数
+ {}.fromkeys(('ss','ss'),300):ss不可变
+ sorted（）:返回列表

##字典使用
+ 键值查找
+ 更新值
+ 添加键值对
+ 判断
+ 删除字典：del 字典
+ 格式化字符串：%（key）格式说明符 % 字典对象名；输出模板  
+ 内建函数：对象名.keys(),对象名.values(),has_key(),对象名.clear()
+ 作为函数形式参数：位置或关键字参数，仅位置参数，可变长位置参数(一个*)：元祖,可变长关键字参数(**):字典

##集合
+ 集合定义：一个无序不重复的元素的组合，可变集合，不可变集合
+ 集合运算：逻辑运算（^对称差分：只属于一个集合）
+ 集合内建函数：面向所有集合，面向可变集合
+ array:shape函数求数组大小

#python扩展库
##扩展库Scipy
+ Numpy
+ SciPy核心库
+ Matplotlib
+ pandas

##ndarry
+ ndarry创建输出：arange(1,5,0.5)
+ ufunc函数：在C语言级别实现，计算很快，能对数组每个元素操作

##Serires
+ 类似一维数对象，由数据索引构成

##Dataframe
+ 一个表格型数据结构
+ 含有一组有序的列（类似index）
+ 可以看成共享同一个index的Series集合
+ ix(a)函数：前a行

#Python数据统计和可视化
##python基本数据统计
###便捷数据获取

###数据准备

###数据显示
+ 显示索引：index(需要注意)
+ 显示列值：columns
+ 显示值：values
+ 显示描述：describe
+ 显示行、切片：head(参数)，tail(参数)

###数据选择
+ 选择行：df[u'2015-03-02'：u'2016-03-02']
+ 选择列：df.列名，df['列名']，df.loc[1:5,],df.loc[1:5,['列名','列名']]，loc使用行列标签
+ 选择区域：iloc使用行列位置
+ 数据筛选：df.[(df.index>=u'2014-04-01')&(df.close>=95)]

###简单统计与处理
+ 均值：mean
+ 差值：diff
+ 排序：sort

###分组grouping
+ df.groupby('month').count()

###merge
+ append追加
+ concat连接:pd.concat([p1,p2],ignore_index=True)
+ join连接:pd.merge(p1,p2,on='连接字段')

##Python高级数据处理和可视化
###聚类分析

###matplotlib图像属性控制

###padas作图
+ 方便快捷：df.close.plot()(对序列和dataframe)
+ 
+ 

###数据存取
+ pd.read_csv('文件')
+ pd.to_scv()
+ pd.to_excel() 


##面向对象
###GUI与面向对象

###抽象
+ 对象（实例）：数据及能对其实施操作所构成的封装体
+ 类：类描述的对象特征（数据和操作）
+ 类的具体化为对象
+ 类的定义:class ClaseName(object):
    'define ClassName class'
     class_suit
+ 类的方法定义：class ClaseName(object):
    'define ClassName class'
     def greet(self)
     print 'Hi!'
+ 类属性：仅仅是所定义的类的变量；创建后使用；类中方法更新，或者主程序中更新；修改属性需要使用类名

###继承
+ 父类、子类
+ 子类定义：class SubClaseName(object):
    'define ClassName class'
     class_suit
+ 私有属性、方法：双下划线（__）单下划线（_）
