# JavaScript 语法错误–函数语句需要名称

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-function-statement-requires-a-name/](https://www.geeksforgeeks.org/javascript-syntaxerror-function-statement-requires-a-name/)

这个 JavaScript 异常**函数语句需要一个名称**，如果脚本中有任何函数语句需要一个名称，就会出现这个异常。

**消息:**

```
Syntax Error: Expected identifier (Edge)
SyntaxError: function statement requires a name [Firefox]
SyntaxError: Unexpected token ( [Chrome]

```

**错误类型:**

```
Syntax Error

```

**错误原因:**代码中任何需要名称的函数语句。只需检查函数是如何定义的，如果需要，请为其提供名称，或者如果所讨论的函数要求是函数表达式，

**例 1:** 本例提供了函数名，所以没有出现错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      var GFG = function () {
        return 'Hello Geek';
      }
      document.write(GFG());
    </script>
</body>
</html>
```

**输出:**

```
Hello Geek

```

**例 2:** 本例未提供函数名，因此出现错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
   <title>Syntax Error</title>
</head>
<body>
    <script>
      function () {
        return 'Hello Geek';
      }
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Function statements require a function name

```