## Exercise 1.1

> 查阅你使用的编译器的文档，确定它使用的文件命名约定。编译并运行第 2 页的 main 程序。

### GCC and File Extensions

| Extension | Meaning | 
| --- | --- |
| .h | C header file (not to be compiled or linked). |
| .c | C source code which must be preprocessed. |
| .i | C source code which should not be preprocessed. |
| .ii | C++ source code which should not be preprocessed. |
| .cc, .cp, .cxx, .cpp, .c++, .C | C++ source code which must be preprocessed. |
| .f, .for, .FOR | Fortran source code which should not be preprocessed. |
| .F, .fpp, .FPP | Fortran source code which must be preprocessed (with the traditional preprocessor). |
| .r | Fortran source code which must be preprocessed with a RATFOR preprocessor (not included with GCC). |
| .s | Assembler code. |
| .S | Assembler code which must be preprocessed. |
| other | An object file to be fed straight into linking. Any file name with no recognized suffix is treated this way. |

 * [GCC and File Extensions](http://labor-liber.org/en/gnu-linux/development/index.php?diapo=extensions) 
 * [File Types Created for Visual C++ Projects](https://msdn.microsoft.com/en-us/library/3awe4781.aspx)

 ## Exercise 1.2

> 改写程序，让它返回 -1。返回 -1 通常被当作程序错误的标识。重新编译并运行你的程序，观察你的系统如何处理 main 返回的错误标识。

```cpp
int main() {
    return -1;
}
```

## Exercise 1.3

> 编写程序，在标准输出上打印 Hello, World

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World" << std::endl;
    return 0;
}
```

## Exercise 1.4

> 我们的程序使用加法运算符+来将两个数相加。编写程序使用乘法运算符*，来打印两个数的积。

```cpp
#include <iostream>

int main() {
    std:cout << "Enter two numbers:" << std::endl;
    int v1 = 0, v2 = 0;
    std::cin >> v1 >> v2;
    std::cout << "The product of " << v1 << " and " << v2 << " is " << v1 * v2 << std::endl;
    return 0;
}
```

## Exercise 1.5

> 我们将所有输出操作放在一条很长的语句中。重写城西，将每个运算对象的打印操作放在一条独立的语句中。

```cpp
#include <iostream>

int main() {
    std:cout << "Enter two numbers:" << std::endl;
    int v1 = 0, v2 = 0;
    std::cin >> v1 >> v2;
    std::cout << "The product of ";
    std::cout << v1;
    std::cout << " and ";
    std::cout << v2;
    std::cout << " is ";
    std::cout << v1 * v2;
    std::cout << std::endl;
    return 0;
}
```
## Exercise 1.6

> 解释下面程序片段是否合法。如果程序是合法的，它输出什么？如果程序不合法，原因何在？应如何修正。

```cpp
std::cout << "The sum of " << v1;
    << " and " << v2;
    << " is " << v1 + v2 << std::endl;
```

程序不合法

**[Error] expected primary-expression before '<<' token**

修复方法：删除多余的 `;`

```cpp
std::cout << "The sum of " << v1 << " and " << v2 << " is " << v1 + v2 << std::endl;
```

## Exercise 1.7

> 编写一个不包含正确的嵌套注释的程序，观察编译器返回的错误信息。

```cpp
/*
* comment pairs /* */ cannot nest.
* ''cannot nest'' is considered source code,
* as is the rest of the program
*/
int main() {
    return 0;
}
```
## Exercise 1.8 

