# 参数列表后的 JavaScript 语法错误(缺失)

> 原文:[https://www . geesforgeks . org/JavaScript-语法错误-参数后缺失-列表/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-after-argument-list/)

如果函数调用中有错误，参数列表后会出现这个 JavaScript 异常**缺失。这可能是键入错误、缺少运算符或未转义的字符串。**

**消息:**

```
SyntaxError: Expected ')' (Edge)
SyntaxError: missing ) after argument list (Firefox)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**在代码的某个地方，函数调用有错误。这可能是键入错误、缺少运算符或未转义的字符串。

**例 1:** 在本例中，字符串串联中缺少一个运算符，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
        var str1 = 'This is ';
        var str2 = 'GeeksforGeeks';
        document.write(str1 str2);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: missing ) after argument list

```

**示例 2:** 在此示例中，有一个未转义的字符串，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
        var str1 = 'This is ';
        var str2 = 'GeeksforGeeks';
        document.write(str1 \str2);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: missing ) after argument list

```