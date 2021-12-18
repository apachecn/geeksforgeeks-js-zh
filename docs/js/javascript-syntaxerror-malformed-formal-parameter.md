# JavaScript 语法错误–格式错误的形式参数

> 原文:[https://www . geesforgeks . org/JavaScript-语法错误-格式错误-形式参数/](https://www.geeksforgeeks.org/javascript-syntaxerror-malformed-formal-parameter/)

如果 Function()构造函数调用的参数列表无效，就会出现这种 JavaScript 异常**格式错误的形式参数**。

**消息:**T0】

**错误类型:**

```
SyntaxError

```

**错误原因:**传递给函数的论点单无效。if 或 var 不能作为参数名，或者参数列表中有一些标点符号。传递的无效值会导致问题，就像数字或对象一样。

**示例 1:** 在本例中，数字用作参数名称。所以错误发生了。

## HTML

```
<script> 
    // error here
    var f = Function(45, "alert('This is alert')"); 
</script>
```

**输出(控制台):**

```
SyntaxError: Expected identifier

```

**例 2:** 本例中缺少逗号，因此出现错误。

## HTML

```
<script>
    var f = Function('x y', 'return x + y;'); 
</script>
```

**输出(控制台):**

```
SyntaxError: Expected ')'

```