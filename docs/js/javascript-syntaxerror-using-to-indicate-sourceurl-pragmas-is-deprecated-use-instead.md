# JavaScript 语法错误–不推荐使用//@来指示 sourceURL pragmas。用//#代替

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-using-to-indicate-source URL-pragmas-is-弃用-use-改为/](https://www.geeksforgeeks.org/javascript-syntaxerror-using-to-indicate-sourceurl-pragmas-is-deprecated-use-instead/)

这个 JavaScript 警告**使用//@来表示 sourceURL pragmas 是不推荐使用的。使用//#代替**如果在 JavaScript 源中定义了源映射语法，而该语法已被折旧，则会出现这种情况。

**消息:**T0】

**错误类型:**

```
This is a warning that a SyntaxError has occurred. 
JavaScript execution won't be halted.

```

**错误原因:**在代码的某个地方，有一个 JavaScript 源中使用的源映射语法，该语法被折旧。

**示例 1:** 在此示例中，sourceURL 与@(已折旧)一起使用。

## HTML

```
<script>
    //@ sourceURL=http://abcd.com/path/name.map
</script>
```

**输出:**

```
Warning: SyntaxError: Using //@ to indicate sourceURL 
         pragmas is deprecated. Use //# instead

```

**示例 2:** 在此示例中，sourceMappingURL 与@(已折旧)一起使用。

## HTML

```
<script>
    //@ sourceMappingURL=http://abcd.com/path/name.map
</script>
```

**输出:**

```
arning: SyntaxError: Using //@ to indicate sourceMappingURL
                     pragmas is deprecated. Use //# instead

```

**参考链接:**[https://developer . Mozilla . org/en-US/docs/Web/JavaScript/Reference/Errors/弃用 _source_map_pragma](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Deprecated_source_map_pragma)