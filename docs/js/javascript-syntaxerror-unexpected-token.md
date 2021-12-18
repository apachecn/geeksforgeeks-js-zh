# JavaScript 语法错误–意外标记

> 原文:[https://www . geesforgeks . org/JavaScript-语法错误-意外-令牌/](https://www.geeksforgeeks.org/javascript-syntaxerror-unexpected-token/)

如果预期会有特定的语言构造，但其他任何东西都被错误地键入，就会出现这种 JavaScript 异常**意外标记**。这可能是一个简单的打字错误。

**消息:**

```
SyntaxError: expected expression, got "x"
SyntaxError: expected property name, got "x" 
SyntaxError: expected target, got "x"
SyntaxError: expected rest argument name, got "x"
SyntaxError: expected closing parenthesis, got "x"
SyntaxError: expected '=>' after argument list, got "x"

```

**错误类型:**

```
SyntaxError

```

**错误原因:**代码中有一个简单的打字错误。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Unexpected Token Error</title>
</head>
<body>
    <script>
        for (let i = 0; i < 5; ++i) {
          document.write(i); 
        }
    </script>
</body>
</html>
```

**输出:**

```
01234

```

**例 2:** 代码中有一个打字错误，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Unexpected Token Error</title>
</head>
<body>
    <script>
        for (let i = 0; i < 5,; ++i) {
          document.write(i); 
        }
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Unexpected token ';'

```