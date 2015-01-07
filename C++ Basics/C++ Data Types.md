##C++中的数据类型##

在任何编程语言中，你需要使用不同的变量来存储各种信息。变量是内存中存储不用数据的预留区域。这意味着，当你创建一个变量的同时，内存也就创建了空间。

你可以存储任何你想像得到的数据，字符、宽字符，整数、浮点数、双精度浮点数，布尔类型等等。

操作系统会根据不同类型的数据决定怎样分配内存，和内存中存储的元素类型。

##原始的内置类型##

C++提供了丰富的内置以及用户定义的数据类型。下面列出了七个基本的数据类型：

    **Type**	            **Keyword**
    Boolean  	               bool
    Character	               char
    Integer  	               int
    Floating point  	       float
    Double floating point	  double
    Valueless	               void
    Wide character	        wchar_t
当然C++也允许出现修饰符：

 1. signed 
 2. unsigned
 3. short 
 4. long

下表显示了变量类型，内存大小以及取值范围。

<table>
<tbody><tr><th>Type</th><th>Typical Bit Width</th><th>Typical Range</th></tr>
<tr><td>char</td><td>1byte</td><td>-127 to 127 or 0 to 255</td></tr>
<tr><td>unsigned char</td><td>1byte</td><td>0 to 255</td></tr>
<tr><td>signed char</td><td>1byte</td><td>-127 to 127</td></tr>
<tr><td>int</td><td>4bytes</td><td>-2147483648 to 2147483647</td></tr>
<tr><td>unsigned int</td><td>4bytes</td><td>0 to 4294967295</td></tr>
<tr><td>signed int</td><td>4bytes</td><td>-2147483648 to 2147483647</td></tr>
<tr><td>short int</td><td>2bytes</td><td>-32768 to 32767</td></tr>
<tr><td>unsigned short int</td><td>Range</td><td>0 to 65,535</td></tr>
<tr><td>signed short int</td><td>Range</td><td>-32768 to 32767</td></tr>
<tr><td>long int</td><td>4bytes</td><td>-2,147,483,647 to 2,147,483,647</td></tr>
<tr><td>signed long int</td><td>4bytes</td><td>same as long int</td></tr>
<tr><td>unsigned long int</td><td>4bytes</td><td>0 to 4,294,967,295</td></tr>
<tr><td>float</td><td>4bytes</td><td>+/- 3.4e +/- 38 (~7 digits)</td></tr>
<tr><td>double</td><td>8bytes</td><td>+/- 1.7e +/- 308 (~15 digits)</td></tr>
<tr><td>long double</td><td>8bytes</td><td>+/- 1.7e +/- 308 (~15 digits)</td></tr>
<tr><td>wchar_t</td><td>2 or 4 bytes</td><td>1 wide character</td></tr>
</tbody></table>

