# JavaScript 课程| JavaScript 中的操作符

> 原文:[https://www . geesforgeks . org/JavaScript-course-operators-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-operators-in-javascript/)

**上一篇文章:** [JavaScript 教程| JavaScript 中的数据类型](https://www.geeksforgeeks.org/javascript-course-data-types-in-javascript/)
一个运算符能够操作某个值或操作数。运算符用于对操作数执行特定的数学和逻辑计算。换句话说，我们可以说一个运算符操作操作数。在 JavaScript 中，运算符用于比较值、执行算术运算等。JavaScript 支持多种运算符:

***   arithmetic operator*   assigning operator*   comparison operator*   logical operator*   ternary operator*   Operator type**

**T21】**

**算术运算符:**
有各种算术运算符–

*   **+(加法):**
    “+”运算符对两个操作数执行加法。
    **例:**

```
Y = 5 + 5 gives Y = 10
```

**注意:**“+”运算符也可以用来连接(添加)字符串。
T3】例:

```
Y = "Geeks" + "for" + "Geeks" gives Y = "GeeksforGeeks"
```

**示例:**

```
Y = "Geeks" + 4 + "Geeks" gives Y = "Geeks4Geeks"
```

*   **–(减法):**
    '-'运算符对两个操作数进行减法运算。
    **例:**

    ```
    Y = 5 - 3 gives Y = 2 
    ```

    *   ***(乘法):**
    “*”运算符对两个操作数执行乘法运算。
    **例:**

    ```
    Y = 5 * 5 gives Y = 25
    ```

    *   **/(除法):**
    '/'运算符对两个操作数进行除法运算(分子除以分母)。
    **例:**

    ```
    Y = 5 / 5 gives Y = 1
    ```

    *   **%(模数):**
    “%”运算符给出一个**整数**除法的余数。
    **例:**

    ```
    A % B means remainder (A/B)
         Y = 5 % 4 gives Y = 1
    ```

    *   **+ +(增量):**
    “++”运算符将整数值增加 1。
    **例:**

    ```
    let A = 10 and Y = A + + then A = 11, Y=10
     if  A = 10 and Y = + + A then A = 11, Y=11
    ```

    *   **–(减量):**
    “-”运算符将整数值减 1。
    **例:**

```
let A = 10 and Y = A - - then A = 9, Y=10
 if  A = 10 and Y = - - A then A = 9, Y=9
```

**赋值运算符:**
JavaScript 中有各种赋值运算符–

*   **=(赋值运算符):**
    将右操作数赋值给左操作数。
    **例:**

    ```
     If A = 10 and Y = A then Y = 10              

    ```

*   **+=(加法和赋值运算符):**
    将左右操作数值相加，然后将结果赋给左操作数。
    **例:**

    ```
    Y += 1 gives Y = Y + 1 
    ```

*   **–=(减法和赋值运算符):**
    它从左侧值中减去右侧值，然后将结果赋给左侧操作数。
    **例:**

    ```
    Y -= 1 gives Y = Y - 1 
    ```

*   类似的还有 ***=(乘法和赋值)**、 **/=(除法和赋值)**、 **%=(模块和赋值)**
    **例:**

    ```
    Y *= A is equivalent to Y = Y * A
    Y /= A is equivalent to Y = Y / A
    Y %= A is equivalent to Y = Y % A

    ```

**比较运算符:**
JavaScript 中有各种比较运算符–

*   **= = :**
    Compares the equality of two operands. If equal then the condition is true otherwise false.
    **Example :**

    ```
    Y = 5 and X = 6
      Y = = X is false.             

    ```

    **注意:**运算符“= =”中未考虑的类型。

*   **= = = :**
    该运算符将两个操作数的相等性与类型进行比较。如果相等(类型和值都相等)，则条件为真，否则为假。
    **例:**

    ```
    given X = 10 then X = = = "10" is false.
    X = = = 10 is true.

    ```

*   **！=(不相等):**
    比较两个操作数的不等式。如果操作数不相等，则为 True。
    **例:**

    ```
    given X = 10 then X ! = 11 is true. 
    ```

*   **>(大于):**
    此运算符检查左侧值是否大于右侧值。如果是，则返回真，否则返回假。
    **例:**

```
given X = 10 then X > 11 is false. 
```

*   **<(小于):**
    此运算符检查左侧值是否小于右侧值。如果是，则返回真，否则返回假。
    **例:**

    ```
    given X = 10 then X < 11 is true. 
    ```

    *   **> =(大于或等于):**
    该运算符检查左侧操作数是否大于或等于右侧操作数。如果是，则返回真，否则返回假。
    **例:**

    ```
    given X = 10 then X > = 11 is false. 
    ```

    *   **< =(小于或等于):**
    该运算符检查左侧操作数值是否小于或等于右侧操作数值。如果是，则返回真，否则返回假。
    **例:**

    ```
    given X = 10 then X < = 10 is true. 
    ```

**typeof Operator:** 在 JavaScript 中，typeof 运算符以字符串的形式返回其操作数的数据类型。操作数可以是任何对象、函数或变量。
**语法:**

```
typeof operand
      OR
typeof (operand)

```

**示例:**

```
<html>
<head>
<title> GfG typeof example </title> 
</head>
<body>

    <script type="text/javascript">
            var a = 17;
            var b = "GeeksforGeeks";
            var c = "";
            var d = null;

            document.write("Type of a = " + (typeof a));
            document.write("<br>");

            document.write("Type of b = " + (typeof b));
            document.write("<br>");

            document.write("Type of c = " + (typeof c));
            document.write("<br>");

            document.write("Type of d = " + (typeof d));
            document.write("<br>");

            document.write("Type of e = " + (typeof e));
            document.write("<br>");
    </script>
</body>
</html>                    
```

**输出:**

```
Type of a = number
Type of b = string
Type of c = string
Type of d = object
Type of e = undefined
```

**下一篇:** [JavaScript 课程|练习小测验-1](https://www.geeksforgeeks.org/javascript-course-quiz-1/)