# 下划线. js _。isNull()功能

> 原文:[https://www . geesforgeks . org/下划线-js-_-isnull-function/](https://www.geeksforgeeks.org/underscore-js-_-isnull-function/)

**_。isNull()函数:**

*   它用于查找对象的值是否为空。
*   如果对象有空值，则输出为真，否则为假。
*   我们甚至可以在这个函数中执行加法、减法等操作。

**语法:**

```
_.isNull(object)
```

**参数:**
只需要一个自变量，就是需要测试的对象。

**返回值:**
如果对象有空值则返回真，否则返回假。

**示例:**

**1。在中传递一个数字。isNull()函数:**
The _。isNull()函数接受传递给它的参数，然后检查对象是否有空值。在这种情况下，由于该值是一个定义的数字“10”，因此输出不为空。因此，输出将为假。

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
        console.log(_.isNull(10));
    </script>
</body>

</html>
```

**输出:**

![](img/09102dbe3f315203c21baed07178a563.png)

**2。将“null”传递给 _。函数:**
既然这里我们已经传递了“空值”，所以我们不需要检查对象。我们知道传递给 _。isNull()函数本身的值为“Null”。因此，输出将为真。

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
        console.log(_.isNull(null));
    </script>
</body>

</html>
```

**输出:**

![](img/dbb6099d2183dba040f056c65e2c113f.png)

**3。将“未定义”传递给 _。isNull()函数:**
The _。isNull()函数接受传递给它的参数，该参数在这里是“未定义的”。我们知道，如果任何东西是未定义的，那么它的值将为空。因此，答案是正确的。

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
        console.log(_.isNull(undefined));
    </script>
</body>

</html>
```

**输出:**

![](img/09102dbe3f315203c21baed07178a563.png)

**4。对的输出执行操作。isNull()函数:**
首先我们把上面两个例子(2，3)的输出直接存储在变量 a 和 b 中，然后我们在两个结果中做了加法运算。最后，将其存储在第三个变量中。自 _ 的输出。isNull()在我们传递时为 false，在我们传递 Null 时为 true，因此 false 存储在“a”变量中，true 存储在“b”变量中。现在，如果我们对‘a’、‘b’变量执行加法(+)运算，那么我们将得到 true，因为‘b’是 true。因此“c”变量将变为 1。

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
        var a = _.isNull(undefined);
        var b = _.isNull(null);
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

**注意:**这些命令在 Google console 或 firefox 中无法工作，因为需要添加这些他们没有添加的附加文件。
所以，添加给定的链接到你的 HTML 文件，然后运行它们。

链接如下:

## 超文本标记语言

```
<!-- Write HTML code here -->
<script type="text/javascript" src =
"https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.9.1/underscore-min.js">
</script>
```