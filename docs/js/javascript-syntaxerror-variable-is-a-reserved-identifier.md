# JavaScript 语法错误“变量”是一个保留的标识符

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-variable-is-a-reserved-identifier/](https://www.geeksforgeeks.org/javascript-syntaxerror-variable-is-a-reserved-identifier/)

这个 JavaScript 异常**变量是一个保留的标识符**如果保留的关键字被用作标识符就会出现。

**消息:**

> 语法错误:标识符使用未来保留字无效(Edge)
> 语法错误:“x”是保留标识符(Firefox)
> 语法错误:意外保留字(Chrome)

**错误类型:**

```
SyntaxError
```

**发生了什么？**

当保留关键字用作标识符时，它们将引发错误。**枚举**在严格和草率模式下都是保留的。而以下关键字在严格模式下被保留。

*   工具
*   包裹
*   公众的
*   连接
*   私人的
*   保护
*   让
*   静电

**例 1:****包**是严格模式下的标识符，所以在这里就可以了。

```
<script>
    var package = "This is GeeksForGeeks"; 
    document.write(package);
</script>
```

**输出:**

```
This is GeeksForGeeks
```

**例 2:****枚举**是一个标识符，所以它会抛出语法错误。

```
<script>
    var enum = "This is GeeksForGeeks"; 
    document.write(enum);
</script>
```

**输出:**

```
SyntaxError: Unexpected reserved word
```