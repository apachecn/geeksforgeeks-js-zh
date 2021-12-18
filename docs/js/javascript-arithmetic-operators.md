# JavaScript |算术运算符

> 原文:[https://www . geesforgeks . org/JavaScript-算术-运算符/](https://www.geeksforgeeks.org/javascript-arithmetic-operators/)

**JavaScript 算术运算符**是对数值进行运算并返回数值的运算符。JavaScript 中有很多运算符。下面描述了每个操作符及其示例。

**1。加法(+)** 加法运算符接受两个数字操作数，并给出它们的数值和。它还连接两个字符串或数字。

**语法:**

```
a + b
```

**示例:**

```
// Number + Number => Addition
1 + 2 gives 3

// Number + String => Concatenation
5 + "hello" gives "5Hello"
```

**2。减法(-)** 减法运算符以数值的形式给出两个操作数的差。

**语法:**

```
a - b
```

**例:**

```
// Number - Number => Subtraction 
10 - 7 gives 3

"Hello" - 1 gives Nan
```

**3。乘法(*)** 乘法运算符给出操作数的乘积，其中一个操作数是被乘数，另一个是乘数。

**语法:**

```
a * b
```

**例:**

```
// Number * Number => Multiplication
3 * 3 gives 9
-4 * 4 gives -16

Infinity * 0 gives NaN
Infinity * Infinity gives Infinity
'hi' * 2 gives NaN
```

**4。除法(/**除法运算符提供其操作数的商，其中右操作数是除数，左操作数是被除数。

**语法:**

```
a / b
```

**例:**

```
// Number / Number => Division
5 / 2 gives 2.5
1.0 / 2.0 gives 0.5

3.0 / 0 gives Infinity
4.0 / 0.0 gives Infinity, because 0.0 == 0
2.0 / -0.0 gives -Infinity
```

**5。模数(%)** 模数运算符返回被除数除以除数后的余数。模数运算符也称为**余数运算符。**它带着红利的符号。

**语法:**

```
a % b
```

**例:**

```
// Number % Number => Modulus of the number

9 % 5 gives 4
-12 % 5 gives -2
1 % -2 gives 1
5.5 % 2 gives 1.5
-4 % 2 gives -0

NaN % 2 gives NaN
```

**6。求幂(**)** 求幂运算符给出将第一个操作数提升到第二个操作数的幂的结果。幂运算子是右关联的。

**语法:**

```
a ** b
```

在 JavaScript 中，不可能写出模棱两可的求幂表达式，也就是说，不能放一元运算符(+/–/~/！/ delete / void)。

**例:**

```
// Number ** Number => Exponential of the number

-4 ** 2 // This is an incorrect expression
-(4 ** 2) gives -16, this is a correct expression
2 ** 5 gives 32
3 ** 3 gives 27
3 ** 2.5 gives 15.588457268119896
10 ** -2 gives 0.01
2 ** 3 ** 2 gives 512

NaN ** 2 gives NaN
```

**7。增量(++)** 增量运算符对其操作数进行增量(加 1)，并返回一个值。

*   If the suffix (for example, x++) is used with the operator after the operand, the value before increment is incremented and returned.
*   If the prefix with operator (for example, ++x) is used before the operand, the incremented value is incremented and returned.

**语法:**

```
a++ or ++a
```

**例:**

```
// Postfix 
var a = 2;
b = a++; // b = 2, a = 3

// Prefix
var x = 5;
y = ++x; // x = 6, y = 6
```

**8。减量(–)**减量运算符对其操作数进行减量(减一)，并返回一个值。

*   If the suffix is used and the operand is followed by an operator (for example, x–), it decrements and returns the value before decrement.
*   If the prefix is used, and the operand is preceded by an operator (for example,–x), it will be decremented, and the decremented value will be returned.

**语法:**

```
a-- or --a
```

**例:**

```
// Prefix
var x = 2;
y = --x; gives x = 1, y = 1

// Postfix 
var x = 3;
y = x--; gives y = 3, x = 2
```

**9。一元(-)** 这是一元运算符，即它对单个操作数进行运算。它给出操作数的否定。

**语法:**

```
-a
```

**例:**

```
var a = 3;
b = -a; gives b = -3, a = 3

// Unary negation operator
// can convert non-numbers
// into a number
var a = "3";
b = -a; gives b = -3
```

**10。一元(+)** 这是一种将非数字转换为数字的方法。虽然一元否定(-)也可以转换成非数字，但一元加号是将某物转换成数字的最快和首选的方式，因为它不对数字执行任何其他操作。

**语法:**

```
+a
```

**例:**

```
+4     gives 4
+'2'   gives 2
+true  gives 1
+false gives 0
+null  gives 0
```