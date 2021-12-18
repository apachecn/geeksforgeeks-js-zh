# JavaScript 语法错误–缺少变量名

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-missing-variable-name/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-variable-name/)

这个 JavaScript 异常**缺少变量名**的情况经常发生，如果名称缺失或者逗号放置错误。可能是打字错误。

**消息:**

```
SyntaxError: missing variable name (Firefox)
SyntaxError: Unexpected token = (Chrome)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**可能有一个变量缺少名称。这是因为代码中的语法错误。逗号可能放在代码的某个地方。

**例 1:** 变量名缺失，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
   <title>Syntax Error</title>
</head>
<body>
    <script>
      var = "This is GeeksforGeeks";
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Unexpected token =

```

**例 2:** 用逗号(，)代替“；”，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
    var var1 = "This is ",
    var var2 = "GFG";
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Unexpected token 'var'

```