# Math.js 编译()函数

> 原文:[https://www.geeksforgeeks.org/math-js-compile-function/](https://www.geeksforgeeks.org/math-js-compile-function/)

Math.js 是一个包含数学函数的扩展库，可以在 JavaScript 和 Node.js 上运行。这个库的附加特性是它提供了一个支持符号计算的灵活的表达式解析器。它非常强大且易于使用，因为它带有许多内置函数，并提供分数、复数、矩阵和单位等数据类型。

**Math.js Compile** 函数用于解析和编译一个表达式。Math.js 编译函数返回一个带有编译表达式的对象，该对象属于 Math.js 求值函数([作用域])。

**语法:**

```
math.compile(expression)     
or                  
math.compile([expression A, expression B, expression C, ...])
```

**参数:**该方法只接受一个参数，如下所述:

*   **表达式:**该参数用于指定需要编译的表达式。

**返回值:**这个方法返回一个带有编译表达式的对象。

**示例 1:**

## HTML

```
<!DOCTYPE HTML>
<html>

<head>
    <!-- specifying the Mathjs source -->
    <script type="text/javascript" 
        src="math.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Defining a constant and calling
        // the compile function
        const a = math.compile('pow(4, 3)')

        // Displaying the output
        document.writeln(" Result = " 
                + a.evaluate());
    </script>
</body>

</html>
```

**输出:**

```
Result = 64
```

**示例 2:**

## HTML

```
<!DOCTYPE HTML>
<html>

<head>
    <!-- specifying the Mathjs source -->
    <script type="text/javascript" 
        src="math.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Defining a scope
        let testScope = { a: 30, b: 5 }

        // Calling the compile function
        const result = math.compile('a/b')

        // Displaying the result
        document.writeln(" Result = "
            + result.evaluate(testScope));
    </script>
</body>

</html>
```

**输出:**

```
Result = 6
```

**示例 3:**

## HTML

```
<!DOCTYPE HTML>
<html>

<head>

    <!-- specifying the Mathjs source -->
    <script type="text/javascript" 
        src="math.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Defining a node and calling 
        // the compile function
        const testNode = math.compile(
            ['a = 12', 'b = 2', 'a / b'])

        // Displaying the result
        document.writeln(" Result = " 
            + testNode[2].evaluate());
    </script>
</body>

</html>
```

**输出:**

```
Result = 6
```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 Math.js 库。