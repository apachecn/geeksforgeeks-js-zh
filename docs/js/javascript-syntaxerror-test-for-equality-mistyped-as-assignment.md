# JavaScript 语法错误–测试等式(==)是否误键入为赋值(=)？

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-test-for-equality-误键入为赋值/](https://www.geeksforgeeks.org/javascript-syntaxerror-test-for-equality-mistyped-as-assignment/)

这个 JavaScript 警告**测试是否相等(==)误键入为赋值(=)？如果用 by 赋值(=)代替等式(==)，则出现**。

**消息:**T0】

**错误类型:**

```
SyntaxError: Warning which is reported only if 
javascript.options.strict preference is set to true.

```

**错误原因:**代码中有一个赋值(=)用来代替等式(==)。

**例 1:** 在本例中，用“=”代替“==”。所以错误发生了。

## HTML

```
<script>
if (a = b) { // Error here
  // do something
}
</script>
```

**输出:**

```
Warning: SyntaxError: test for equality (==) 
mistyped as assignment (=)?

```

**例 2:** 在本例中，用“=”代替“==”。所以错误发生了。

## HTML

```
<script>
    var a = 5;
    var b = 4;
    var c = 5;
    if (b = c) {
      // do something
    } else if (a = c) {
      // do something
    }
</script>
```

**输出:**

```
Warning: SyntaxError: test for equality (==) 
mistyped as assignment (=)?

```