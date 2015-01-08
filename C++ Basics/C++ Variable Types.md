##C++中的变量类型##

变量是C++提供的一个程序可通过名称操控的存贮区域。在C ++中的每个变量具有特定的类型，变量决定了占用内存的大小和在内存中存放的方式;该存储区域内可存放一定范围的变量;也可通过程序改变属性。

The name of a variable can be composed of letters, digits, and the underscore character.

变量的名称可以包含字母，数字和下划线。开头必须是字母或者下划线。注意变量的名称区分大小写。

下表具体的解释了不同的变量类型以及描述。

<table class="src">
<tbody><tr><th width="30%">类型</th><th>藐视</th></tr>

<tr><td>bool</td><td>存贮一个为“真”或“假”的值.</td></tr>

<tr><td>char</td><td>存贮<b>一个</b>字符。这是一个整型变量.</td></tr>

<tr><td>int</td><td>存储自然数</td></tr>

<tr><td>float</td><td>单精度的小数</td></tr>

<tr><td>double</td><td>双精度小数</td></tr>

<tr><td>void</td><td>代表不存在类型</td></tr>

<tr><td>wchar_t</td><td>宽字符类型</td></tr>

</tbody></table>

C ++也允许定义各种其他类型的变量，像枚举，指针，数组，引用，数据结构和类。这些将在后面的章节中进行解释。

下个部分将描述如何在C++中定义，声明和使用不同类型的变量。

##C++中变量的定义##

变量定义是指，高速编译器在哪里，创建多少内存来存储变量。变量的定义就是一个数据类型。后面跟着的是变量的名称，可以是一个，亦可以是多个。就像下面这样：

    type variable_list;


Here, type must be a valid C++ data type including char, w_char, int, float, double, bool or any user-defined object, etc.,

这里的”类型（type）“必须是一个有效的C++数据类型，包含字符，宽字符，整型，单精度和双精度、布尔值以及其他用户定义的类型等等。

and variable_list may consist of one or more identifier names separated by commas. Some valid declarations are shown here

变量列表（variable_list ）必须包含一个或多个变量的名称，用逗号分隔开。以下是一些例子：

    int    i, j, k;
    char   c, ch;
    float  f, salary;
    double d;


在"int i,j,k;"这行语句中，定义和声明了名称为"i,.j,k"的变量。这就告诉了编译器要创建三个名称分别为”i,j,k“的整形变量。

变量在其声明时可被初始化”给变量赋值“。初始化时，变量的后面加上”=“接着是其需要初始化的值。如下：

    type variable_name = value;

这里也有一些其他的例子：

    extern int d = 3, f = 5;    // 声明并初始化d和f. 
    int d = 3, f = 5;           // 定义并初始化d,f. 
    byte z = 22;                // 定义并初始化z. 
    char x = 'x';               // X变量中存储了'x'这个字符.

对于定义了尚未初始化的变量，如果是静态变量的话，会初始为NULL。（所有的字节值为0）。对于其他类型的变量，没有初始化的值是不确定的。

#C++变量的声明#


变量的声明就是告诉编译器又一个给定类型和名称的变量存在，编译器由此可进一步的编译程序而不细变量的详细信息和值。

变量的声明只有在其编译时期才有意义，在编译器链接程序的时候需要实际的变量声明。


