# JavaScript 语法错误:未终止的字符串文字

> 原文:[https://www . geesforgeks . org/JavaScript-语法错误-未终止-字符串-文字/](https://www.geeksforgeeks.org/javascript-syntaxerror-unterminated-string-literal/)

如果存在未正确终止的字符串，则会出现此 JavaScript 错误**未终止的字符串文字**。字符串必须用单引号(')或双引号(")括起来。

**消息:**

```
SyntaxError: Unterminated string constant (Edge)
SyntaxError: unterminated string literal (Firefox)

```

**错误类型:**

```
SyntaxError
```

**发生了什么？**

代码中有一个字符串没有被终止。字符串需要用单引号(')或双引号(")括起来。JavaScript 认为单引号字符串和双引号字符串没有区别。

**示例 1:** 在本例中，使用了单引号，字符串没有终止，因此出现了错误。

```
<!DOCTYPE html>
<html>
<head>
<title>Syntax Error</title>
</head>
<body>
    <script>
    var GFG_str = 'This
                     is 
                     GeeksForGeeks';
    document.write(GFG_str);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Unterminated string constant

```

**例 2:** 本例中使用了双引号，字符串没有终止，所以出现了错误。

```
<!DOCTYPE html>
<html>
<head>
<title>Syntax Error</title>
</head>
<body>
    <script>
    var GFG_str = "This
                     is 
                     GeeksForGeeks";
    document.write(GFG_str);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Unterminated string constant

```