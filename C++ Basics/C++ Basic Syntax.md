##C++的基本语法##

当我们设计一个C++程序时，可以看作是类之间相互调用方法来通信的集合。现在，让我们大概看看什么是类，对象，方法和实例变量。

 - **对象** 对象有基本的属性跟行为：例如，狗有名字、颜色、等等这些基本的属性。狗的行为包含睡觉，吃（汪星人：我不是猪）....。一个对象就是一个实例化的类。比如有一直叫做“ex0”的狗，这个“ex0”就是一个对象。而“狗”就是这个对象所属的类。
 - **类（class)** .类就是一个只有描述(包括属性，行为)。没有具体定义的“对象”。
 - **Methods（有些人叫方法，有些人叫函数）**。函数是一个类的行为描述，在程序中通常可以写逻辑代码，操作数据和执行特定的动作。
 - **实例变量（Instance Variables)** 。每个对象都有一套独特的实例变量。并且当前对象的属性是通过分配给实例变量的值来创建的。


##C++程序结构:##

先来看一段简单的Hello world程序：

     #include <iostream>
    using namespace std;
    
    // main() 函数是程序的入口
    
    int main()
    {
       cout << "Hello World"; // 打印出hello world。
       return 0;
    }

看看究竟一个C++的程序都有啥？</br>


这段代码首先定义了头部信息包含一个include定义，这表示需要引入外部文件。而这个文件是iostream。在c++的库目录中存在，所有用的是“<>”。如果需要引入一个不再库中的文件需要使用双引号（英文的双引号）。

第二行 using namespace std; 告诉编译器要引入一个名字叫做”std“的命名空间。命名空间是c++相对于c的一个新特性。

下一行以“//”开头。表示这是一个注释语句，c++就会自动忽略这行代码。//就像我忽略环境设置这一章一样...

int main() 这一行定义了这段代码的入口，所有的c++程序都是从main函数执行的。需要注意的是。在c++中的main函数**必须是int 类型**的（当然有的编译器允许你采用c中的（void）类型。

下一行中的 cout<<"hello world";会在屏幕上显示出hello world这句话。

下一行的 return 0;表示终止main函数并且给调用main函数的进程返回一个0。

##编译&执行c++程序##

接下来是如何保存，编译和执行c++程序。

1.首先打开一个文本编辑器（强烈反对你用记事本）。并把上方的代码输入进去。保存为"hello.cpp"。

2.打开终端，并进入到你所保存文件的目录下。

3.输入命令“g++ hello.cpp” 按下回车来编译你的程序。如果程序没有错误的话在下一行会给你一个"xx.out"的提示，并生成这个文件。

4.现在执行“./a,out” 来运行你的程序。

5.屏幕上会显示“hello world”。

PS:确定你已经设置好了环境变量在执行以上操作。如果你懒得设置的话，下载一个IDE也是一个不错的选择。比如code::blocks 。或者微硬出品的VS系列亦可。当然如果懒得装这些东西的话，在[这里][1]也可运行。

##分号和代码块##
分号“;”表示c++一个语句的结束，也就是每条c++语句结束之后都必须加上一个分号。它表示这一个逻辑的结束。

例如，下面这些语句

    x = y;
    y = y+1;
    add(x, y);

代码块是被一对大括号“｛｝”括起来的几条语句。通常这些语句的逻辑有相关性。

例如：

       {
       cout << "Hello World"; // prints Hello World
       return 0;
     }

c++不以换行作为语句结束的标志，一句话可以在一行，也可以在多行。而一行也同样可以有多个语句，例如：

    x = y;
    y = y+1;
    add(x, y);

和下面这个代码等价：

    x = y; y = y+1; add(x, y);
    
##C++的标识符##
C++的标识符可用作命名（区分）变量，函数，结构，类，模块等等和其他用户定义元素。一个合法的标识符以 字母或者下划线_开头。后面可以跟一个或多个的数字、字母下划线。C++不允许标识符中混入奇怪的东西（特殊符号）。比如@#！￥%这些虽然可用作表示吐槽，可不能在c++中用作标识符。ATTENTION：c++的标识符是区分大小写的。比如QQ和qq就是两个不同的标识符。
下面是一些合法的标识符：

    mohd       zara    abc   move_name  a_123
    myname50   _temp   j     a23b9      retVal
    
##C++的关键字##
 
C++中的关键字不能用作标识符，下面是C++的关键字列表：

    asm	else	new	this
    auto	enum	operator	throw
    bool	explicit	private	true
    break	export	protected	try
    case	extern	public	typedef
    catch	false	register	typeid
    char	float	reinterpret_cast	typename
    class	for	return	union
    const	friend	short	unsigned
    const_cast	goto	signed	using
    continue	if	sizeof	virtual
    default	inline	static	void
    delete	int	static_cast	volatile
    do	long	struct	wchar_t
    double	mutable	switch	while
    dynamic_cast	namespace	template
   
##Trigraphs(三字母序列)##

这段古老的历史就由下面这位讲讲吧：

http://blog.sina.com.cn/s/blog_4b687eac01008ice.html

##C++中的空白字符##

仅包含空格，（制表符）的一行叫做“空行”。C++在编译时期会忽略这行代码（加了注释也没用）


空白字符是C++用来描述空格，制表符，换行符和注释的术语。空白字符在声明中可以分离数据类型和标识符，使编译器能够找声明了的元素，如int的结束和下一个元素开始。因此，在声明，

    int age;

中，在int和age中间必须加上一个空白字符。使编译器能找到age这个元素并定义为int类型。

另一方面：又如，下面这个语句：

    fruit = apples + oranges;   // Get the total fruit
    

在"fruit = apples" 和 “apples + oranges"的等号与加号中间加了空格，会显得代码更为清晰。（当然你亦可以不加，省了大概十分之一颗糖的能量）


  [1]: http://www.tutorialspoint.com/cplusplus/try_cplusplus.php
