# JavaScript 语法错误–缺失；声明前

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-missing-before-statement/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-before-statement/)

此 JavaScript 异常**缺失；如果有分号(；)在脚本中缺失。**

**消息:**

```
SyntaxError: Expected ';' (Edge)
SyntaxError: missing ; before statement (Firefox)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**代码中某处缺少分号(；).您需要提供它，以便 JavaScript 可以解析源代码而没有任何错误。

**示例 1:** 在本例中，字符串没有被正确转义，JavaScript 需要一个“；”，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
        // invalid string
        var GFG = 'This is GFG's platform';  
        document.write(GFG);
    </script>
</body>
</html>
```

**输出(在边缘浏览器的控制台中):**

```
SyntaxError: Expected ';'

```

**示例 2:** 在本例中，对象的属性是用 var 声明声明的，这是无效的。所以错误发生了，

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
        var GFG = {};
        var GFG.prop_1 = 'Val_1';  
        document.write(JSON.stringify(GFG));
    </script>
</body>
</html>
```

**输出(在边缘浏览器的控制台中):**

```
SyntaxError: Expected ';'

```