《简明Python教程》这本书是初级的Python入门教材，初级的内容基本覆盖，对高级的内容没有做深入纠结。适合刚接触Python的新手，行文比较简洁轻松，读起来也比较顺畅。
下面是我根据各个章节的内容进行的简要归纳，相关代码都已按照章节顺序进行命名。

- Python介绍

    简单、易学、免费、开源、可移植性好、面向对象、可扩展、丰富的库等等

- Python安装

    linux系统：判断是否安装 python -v

    Windows系统： 下载软件安装即可

- 最初的步骤

    挑选合适的编辑器。\n

    \#符号右面的内容都是注释

    Linux系统下运行：chmod a+x helloworld.py

    echo $PATH 来显示PATH变量

    help()帮助了解命令含义 q退出

- 基本概念

    数：整数、长整数、浮点数和复数。

    字符串:""",转义符，Unicode字符。

    标识符命名：大小写敏感、字母数字下划线（开头不能有数字）

    逻辑行：用；隔开，清晰理解。

- 运算符和表达式

    位运算 左移、右移、位与、位或、位异或

    运算符优先级

- 控制流

    if、while、for、break、continue

- 函数

    形参与实参。调用函数时，实参值赋给形参。

    局部变量：函数内部定义的变量与外部完全没有关系。产生效果的区域成为局部作用域。

    全局变量：定义全局变量。在函数内部使用global语句。（不推荐）

    默认参数值：def func(a, b=5)是有效的，但是def func(a=5, b)是 无效的。

    关键参数：我们可以只给我们想要的那些参数赋值。

    return语句：没有返回值的return语句等价于return None。None是Python中表示没有任何东西的特殊类型。

    文档字符串：方便程序的阅读理解。

- 模块

    sys模块：sys模块包含了与Python解释器和它的环境有关的函数。

    .pyc文件: 字节编译的文件 ，这些文件以.pyc作为扩展名。

    from..import语句: from sys import argv语句。

    模块的__name__：获取模块的名称。__main__为当前程序。

    制造你自己的模块：记住这个模块应该被放置在我们输入它的程序的同一个目录中，或者在sys.path所列目录之一。

    dir()：内建的dir函数来列出模块定义的标识符。标识符有函数、类和变量。

- 数据结构

    列表：len(list)、list.append、list.sort、del list[0]

    元组：元组和字符串一样是不可变的，即你不能修改元组。元组通过圆括号中用逗号分割的项目定义。

    字典：它们的键/值对用冒号分割，而各个对用逗号分割，所有这些都包括在花括号中。

        赋值：d[key]= value

        删除：del d[key]

        迭代出每一项：for name,address in ab.items():

    序列：列表、元组、字符串都属于序列。序列的两个特点：索引操作符和切片操作符。

        引用：当你创建一个对象并给它赋一个变量的时候，这个变量仅仅 引用 那个对象，而不是表示这个对象本身！

        字符串方法: in操作符用来检验一个给定字符串是否为另一个字符串的一部分。

        find方法用来找出给定字符串在另一个字符串中的位置，或者返回-1以表示找不到子字符串。

        str类也有以一个作为分隔符的字符串join序列的项目的整洁的方法，它返回一个生成的大字符串。

- 面向对象编程

    self:类的方法与普通的函数只有一个特别的区别——它们必须有一个额外的第一个参数名称，但是在调用这个方法的时候你不为这个参数赋值，Python会提供这个值。这个特别的变量指对象本身，按照惯例它的名称是self。

    __init__方法: __init__方法在类的一个对象被建立时，马上运行。这个方法可以用来对你的对象做一些你希望的初始化 。

    类与对象的方法：类的变量 由一个类的所有对象（实例）共享使用。对象的变量 由类的每个对象/实例拥有。

    继承：基本类的__init__方法专门使用self变量调用。

- 输入输出

    模式可以为读模式（'r'）、写模式（'w'）或追加模式（'a'）。

    使用file类的write方法来写文件，最后我们用close关闭这个文件。

    使用readline方法读文件的每一行。

    存储与去存储没看懂。

- 异常

    用try..except语句来处理异常。

    用raise来引发异常。

    try...finally异常发生后有语句仍然执行。

- python标准库

    sys模块、os模块。

- 更多python内容

    __init__(self, ...)、__del__(self)、__str__(self)、__lt__(self, other)、__getitem__(self, key)、__len__(self)

    列表生成式、单语句块、lambda语句

    exec语句用来执行储存在字符串或文件中的Python语句：
    \>>> exec 'print "Hello World"

    eval语句用来计算存储在字符串中的有效Python表达式。
    \>>> eval('2*3')

    assert语句用来声明某个条件是真的。当assert语句失败的时候，会引发一个AssertionError。

    repr函数

