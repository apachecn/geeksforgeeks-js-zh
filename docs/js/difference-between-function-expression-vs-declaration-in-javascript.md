# 函数表达式与 JavaScript 中声明的区别

> 原文:[https://www . geesforgeks . org/function-expression-vs-declaration-in-JavaScript/](https://www.geeksforgeeks.org/difference-between-function-expression-vs-declaration-in-javascript/)

**函数声明:**
A **函数声明**(或函数语句)用指定的参数定义函数，不需要变量赋值。它们独立存在，即它们是独立的构造，不能嵌套在非功能块中。使用*函数*关键字声明一个函数。

*   **语法:**

    ```
    function gfg(parameter1, parameter2) {
     //A set of statements
     }

    ```

**函数表达式:**
A **函数表达式**的工作方式就像函数声明或者函数语句一样，唯一的区别就是函数名不是在函数表达式中开始的，即*匿名函数*是在函数表达式中创建的。函数表达式一定义就运行。

*   **语法:**

```
var gfg = function(parameter1, parameter2) {
 //A set of statements
 }

```

**示例 1:** 使用函数声明

```
<!DOCTYPE html>
<html>

<head>
    <title>Function Declaration</title>
</head>

<body>
    <center>
        <h1 style="color:green">GeeksforGeeks</h1>
        <h3>Function Declaration</h3>
        <script>
            function gfg(a, b) {
                return a * b;
            }
            var result = gfg(5, 5);
            document.write(result);
        </script>
    </center>
</body>

</html>
```

**输出:**

```
25

```

**示例 2:** 使用函数表达式

```
<!DOCTYPE html>
<html>

<head>
    <title>Function Expression</title>
</head>

<body>
    <center>
        <h1 style="color:green">GeeksforGeeks</h1>
        <h3>Function Expression</h3>
        <script>
            var gfg = function(a, b) {
                return a * b;
            }
            document.write(gfg(5, 5));
        </script>
    </center>
</body>

</html>
```

**输出:**

```
25

```