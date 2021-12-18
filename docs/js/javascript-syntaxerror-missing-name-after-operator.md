# JavaScript 语法错误–后面缺少名称。操作员

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-运算符后缺少名称/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-name-after-operator/)

此 JavaScript 异常**后面缺少名称。运算符**如果点运算符(。)以错误的方式用于属性访问。

**消息:**

```
SyntaxError: missing name after . operator

```

**错误类型:**

```
SyntaxError

```

**错误原因:**点运算符(。)用于访问属性。用户必须提供要访问的属性的名称。在某些地方，点运算符与方括号一起使用，或者“+”与点运算符一起使用，两者都会导致问题。

**示例 1:** 在本例中，使用点运算符和方括号访问属性，因此出现了错误。

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
      prop: 
       { 
        prop1: "val1", 
        prop2: "val2" 
       }
    };
    document.write(GFG_Obj.[prop].[prop1]);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: missing name after . operator

```

**示例 2:** 在本例中，属性是用点运算符和“+”(串联)一起访问的，因此出现了错误。

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
      prop: 
       { 
        prop1: "val1", 
        prop2: "val2" 
       }
    };
    var k = 2;
    document.write(GFG_Obj.prop."prop" + k);
    </script>
</body>
</html>
```

**输出(控制台中):**

```
SyntaxError: missing name after . operator

```