## Exercise 2.1

> 类型 int、long、long long 和 short 的区别是什么？无符号类型和带符号类型的区别是什么？float 和 double 的区别是什么？

C++ 语言规定，一个 `int` 至少和 `short` 一样大，一个 `long` 至少和一个 `int` 一样大，一个 `long long` 至少和一个 `long` 一样大。

带符号型可以标识正数，负数或 0，无符号型只能标识大于等于 0 的值。

`float` 是单精度浮点型，`double` 是双精度浮点型

使用的时候：
1. 当明确知晓不可能为负时，选用无符号类型。
2. 使用 int 执行整数运算。实际使用中 short 常常显得太小而 long 一般和 int 有相同的尺寸。如果你的数值超过了 int 的标识范围，选用 long long。
3. 在算数表达式中不要使用 char 或 bool，只有在存放字符和布尔值的时候才使用它们。因为 char 类型在一些机器上是有符号的，而在另一些机器上是无符号的。如果需要使用一个不大的整数，那么明确指出它的类型是 signed char 或者 unsigned char。
4. 执行浮点数运算选用 double, 这是因为 float 通常精度不够而且双精度浮点数和单精度数的计算代价相差无几。事实上，对于某些机器来说，双精度运算甚至比单精度还快。long double 提供的精度在一般情况下是没有必要的，况且它带来的运行消耗也不容忽视。
 
## Exercise 2.2

> 计算按揭贷款时，对于利率、本金和付款分别应选择何种数据类型？说明你的理由。

都应该是用 double 或者 float。

## Exercise 2.3

> 读程序写结果

```cpp
unsigned u = 10, u2 = 42;
std::cout << u2 - u << std::endl;
std::cout << u - u2 << std::endl;

int i = 10, i2 = 42;
std::cout << i2 - i << std::endl;
std::cout << i - i2 << std::endl;
std::cout << i - u << std::endl;
std::cout << u - i << std::endl;
```

```
32
4294967264
32
-32
0
0
```

## Exercise 2.4

> 编程检查你的估计是否正确，如果不正确，请自己研读本节直到弄明白问题的所在。

