# 元素列表

后的 JavaScript 语法错误–缺失】

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-元素后缺失列表/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-after-element-list/)

元素列表后出现这个 JavaScript 异常**缺失，可能是代码中数组初始化语法错误。缺少右括号(“]”)或逗号(“，”)也会引发错误。**

**消息:**

```
SyntaxError: missing ] after element list

```

**错误类型:**

```
SyntaxError

```

**错误原因:**在脚本的某个地方，数组初始化语法有错误。缺少右括号(“]”)或逗号(“，”)会产生问题。

**示例 1:** 在本例中，数组声明中缺少“]”。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      var arr = [1, 2,                  
      document.write(arr);
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
SyntaxError : Expected ']'

```

**示例 2:** 在本例中，数组声明中缺少“，”。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      var GFG_Obj = [{prop_1: 'val_1'} {prop_2: 'val_2'}];                      
      document.write(GFG_Obj);
    </script>
</body>
</html>
```

**输出(在边缘控制台** ) **:**

```
SyntaxError : Expected ']'

```