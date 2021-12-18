# JavaScript 操作符

> 原文:[https://www.geeksforgeeks.org/javascript-operators/](https://www.geeksforgeeks.org/javascript-operators/)

下面是基本比较运算符的示例。

**例 1:**

## java 描述语言

```
<script>
    function gfg() {
    let val1 = 5;
    // Equality Operators
    document.write(val1 == 5);
    document.write("<br>");
    // Relational Operators
    document.write(val1 > 0);
    }
    gfg();
</script>
```

**输出:**

```
true
true
```

运算符能够操作某个值或操作数。运算符用于对操作数执行特定的数学和逻辑计算。换句话说，我们可以说一个运算符操作操作数。在 JavaScript 中，运算符用于比较值、执行算术运算等。JavaScript 支持多种运算符:

*   **算术运算符**
*   **比较运算符**
*   **逻辑运算符**
*   **分配操作员**
*   **三元运算符**
*   **操作员类型**

**算术运算符:**
有各种算术运算符–

*   **+(加法):**
    “+”运算符对两个操作数执行加法。
    **例:**

```
Y = 5 + 5 gives Y = 10
```

*   **注意:**“+”运算符也可以用来连接(添加)字符串。
    T3】例:

```
Y = "Geeks" + "for" + "Geeks" gives Y = "GeeksforGeeks"
```

*   **示例:**

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
    “*”运算符对两个操作数进行乘法运算。
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

*   **= = =:**
    比较两个操作数的相等性。如果相等，则条件为真，否则为假。
    **例:**

```
Y = 5 and X = 6
  Y = = X is false.             

```

*   **注意:**运算符“= =”中未考虑的类型。

*   **= = = :**
    这个运算符比较两个操作数的相等性和类型。如果相等(类型和值都相等)，则条件为真，否则为假。
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

**逻辑运算符:**
JavaScript 中有各种各样的逻辑运算符–

*   **& &(逻辑与):**
    它检查两个操作数是否非零(0、假、未定义、空或""被认为是零)，如果是，则返回 1，否则返回 0。
    **例:**

```
Y = 5 and X = 6
Y && X is true.
```

*   **||(逻辑 OR) :**
    它检查两个操作数中是否有任何一个非零(0、假、未定义、空或""被认为是零)。因此||如果任一操作数为真，则返回真；如果两个操作数都为假，则返回假。
    **例:**

```
Y = 5 and X = 0
Y || X is true.
```

*   **！(逻辑非):**
    它反转操作数(或条件)的布尔结果。
    **例:**

```
Y = 5 and X = 0
!(Y || X) is false.
```

**三元运算符:**

*   **:？运算符:**
    它类似于 if-else 条件的缩写。
    **语法:**

```
Y =  ? A : B 
```

*   其中 A 和 B 是值，如果条件为真，则 Y = A，否则 Y = B。
    **示例:**

```
Y = (6>5) ? 6 : 5
therefore Y = 6
```

*   **运算符的类型:**它返回变量的类型。
    **语法:**

```
typeof variable;
```

**示例:**

## java 描述语言

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

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。