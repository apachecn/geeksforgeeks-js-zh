# 下划线. js _。isNaN()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-isnan-function/](https://www.geeksforgeeks.org/underscore-js-_-isnan-fucntion/)

**_。isNaN()功能:**

*   它用于查找传递的对象的值是否为 NaN。
*   如果对象的值是 NaN，则输出为真，否则为假。
*   我们甚至可以在这个函数中执行加法、减法等操作。

**语法:**

```
_.isNaN(object)
```

**参数:**
只需要一个参数，就是需要检查的对象。
**返回值:**
如果对象的值为 NaN 则返回 true，否则返回 false。
**示例:**

*   **将数字传递给 _。isNan()函数:**
    The _。isNaN()函数接受传递给它的元素，并检查它的值是否为 NaN。因为一个数字被传递，我们知道这个数字有自己的值，所以输出会是假的。

## 超文本标记语言

```
<!-- Write HTML code here -->
<html>

<head>
    <script src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js" >
    </script>
</head>

<body>
    <script type="text/javascript">
        var a=10;
        console.log(_.isNaN(10));
    </script>
</body>

</html>
```

**输出:**

![](img/09102dbe3f315203c21baed07178a563.png)

*   **传递‘NaN’到 _。isNan()函数:**
    由于这一次，Nan 本身被传递给了函数，所以，当函数检查时，它发现传递的变量有 Nan 值。Ans 因此，输出将为真。

## 超文本标记语言

```
<!-- Write HTML code here -->
<html>

<head>
    <script src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js" >
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(_.isNaN(NaN));
    </script>
</body>

</html>
```

**输出:**

![](img/dbb6099d2183dba040f056c65e2c113f.png)

*   **将“未定义”传递给 _。isNaN()函数:**
    The _。isNaN()函数接受这里是“未定义”的参数并开始检查。我们知道，“未定义”没有任何值，因此它的值肯定不是 NaN。所以，答案是假的。

## 超文本标记语言

```
<!-- Write HTML code here -->
<html>

<head>
    <script src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js" >
    </script>
</head>

<body>
    <script type="text/javascript">
        console.log(_.isNaN(undefined));
    </script>
</body>

</html>
```

**输出:**

![](img/09102dbe3f315203c21baed07178a563.png)

*   **对 _ 的输出进行运算。isNan()函数:**
    这里，我们使用上面解释的示例 2 和示例 3。然后将它们的值存储在变量“a”和“b”中。因此，变量“a”为假，“b”为真。最后，我们对“a”和“b”执行“或”运算，并将结果存储在变量“c”中。既然‘b’是真的，那么‘c’就是 1。

## 超文本标记语言

```
<!-- Write HTML code here -->
<html>

<head>
    <script src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js" >
    </script>
</head>

<body>
    <script type="text/javascript">
        var a = _.isNaN(undefined);
        var b = _.isNaN(NaN);
        var c = a + b;
        console.log(a);
        console.log(b);
        console.log(c);
    </script>
</body>

</html>
```

**输出:**

![](img/b2e0aeddc160e2c9d2447a244f8b325f.png)

**注意:**
这些命令在 Google 控制台或 firefox 中无法工作，因为这些额外的文件需要添加，而它们没有添加。
因此，将给定的链接添加到您的 HTML 文件中，然后运行它们。
链接如下:

## 超文本标记语言

```
<!-- Write HTML code here -->
<script type="text/javascript" src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
</script>
```