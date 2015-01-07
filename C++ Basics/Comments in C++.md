##C++中的注释##

程序注释是代码的解释说明。写出来帮助其他人阅读你写的源码。所有的编程语言都支持注释。

C ++支持单行和多行注释。任何注释中的内容编译器都会忽略。

C ++的多行注释由/*开始和结束于*/。例如：

      /* This is a comment */
    
    /* C++ comments can  also
     * span multiple lines
     */
单行注释以//开头，例如：

    #include <iostream>
    using namespace std;
    
    main()
    {
       cout << "Hello World"; // prints Hello World
    
       return 0;
    }
上方代码在编译时期会忽略  // prints Hello World 。并输出以下结果：

    Hello World
在/* */注释中//没有其他含义，因此你可以在/* */注释中混合使用//注释，比如：

    /* Comment out printing of Hello World:
    
    cout << "Hello World"; // prints Hello World
    
    */
