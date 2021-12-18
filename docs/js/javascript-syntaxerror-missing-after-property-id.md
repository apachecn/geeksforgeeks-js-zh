# JavaScript 语法错误–属性 id

后缺少“:”

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-property-id 后缺失/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-after-property-id/)

这个 JavaScript 异常**缺失:如果使用对象的初始化语法声明对象，则在属性 id** 之后出现。

**消息:**

```
SyntaxError: Expected ':' (Edge)
SyntaxError: missing : after property id (Firefox)

```

**错误类型:**

```
SyntaxError

```

**错误原因:**在代码中的某个地方，对象是用对象初始值设定项语法创建的，冒号(:)用于分隔对象属性的键和值，但实际上并没有这样使用。

**例 1:** 本例中用“=”代替“:”，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
        var GFG_Obj = { 
            // invalid syntax
            key = 'value' 
        };
        document.write(JSON.stringify(GFG_Obj));
    </script>
</body>
</html>
```

**输出(在边缘浏览器的控制台中):**

```
SyntaxError: Expected ':'

```

**示例 2:** 在此示例中，对象的键缺少值，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      // invalid syntax
      var GFG_Obj = { key; };  
      document.write(JSON.stringify(GFG_Obj));
    </script>
</body>
</html>
```

**输出(在边缘浏览器的控制台中):**

```
SyntaxError: Expected ':'

```