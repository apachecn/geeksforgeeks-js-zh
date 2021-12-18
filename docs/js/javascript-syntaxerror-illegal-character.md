# JavaScript 语法错误–非法字符

> 原文:[https://www . geesforgeks . org/JavaScript-语法错误-非法-字符/](https://www.geeksforgeeks.org/javascript-syntaxerror-illegal-character/)

如果代码中有一个不属于那里的无效或意外的标记，就会出现这个 JavaScript 异常**非法字符**。

**消息:**

```
SyntaxError: Invalid character (Edge)
SyntaxError: illegal character (Firefox)
SyntaxError: Invalid or unexpected token (Chrome)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**代码中有一个无效或意外的令牌不属于那里。检查代码中的不匹配，如减号(–)和破折号(–)或简单引号( " )与非标准引号(")。

**例 1:** 在本例中，不存在任何不匹配，因此没有出现错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      // Valid token
         var GFG_colors = ['#002', '#353', '#665']; 
      document.write(GFG_colors)
    </script>
</body>
</html>
```

**输出:**

```
#002,#353,#665

```

**示例 2:** 在本例中，存在令牌不匹配，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      // Invalid Token
      var GFG_colors = ['#002', '#353', '#665']; 
      document.write(GFG_colors)
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Invalid or unexpected token

```