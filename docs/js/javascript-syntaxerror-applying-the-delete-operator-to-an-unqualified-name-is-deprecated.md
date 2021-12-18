# JavaScript 语法错误–对非限定名称应用“删除”运算符已被否决

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-将-delete-operator 应用于不合格名称-已弃用/](https://www.geeksforgeeks.org/javascript-syntaxerror-applying-the-delete-operator-to-an-unqualified-name-is-deprecated/)

将“删除”操作符应用于非限定名称的 JavaScript 异常**不推荐使用**在严格模式下工作，如果试图用**删除操作符删除变量，就会出现这种情况。**

**消息:**

```
SyntaxError: Calling delete on expression not allowed
             in strict mode (Edge)
SyntaxError: applying the 'delete' operator to an unqualified name
             is deprecated (Firefox)
SyntaxError: Delete of an unqualified identifier in strict mode. 
             (Chrome)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**在严格模式下，试图删除一个变量会抛出错误，是不允许的。JavaScript 中的普通变量不能在 delete 操作符的帮助下删除。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      'use strict';
      var GFG ="This is GeeksforGeeks";
      document.write(GFG);
      GFG = null; 
    </script>
</body>
</html>
```

**输出:**

```
This is GeeksforGeeks

```

**例 2:** 在本例中，使用了导致错误的 delete 运算符。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      'use strict';
      var GFG ="This is GeeksForGeeks";
      document.write(GFG);
      delete GFG; 
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: Delete of an unqualified identifier in strict mode.

```