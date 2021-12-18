# JavaScript 语法错误–“0”前缀的八进制文字和八进制转义序列被弃用

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-0-前缀-八进制-文字-和-八进制-转义序列-不推荐使用/](https://www.geeksforgeeks.org/javascript-syntaxerror-0-prefixed-octal-literals-and-octal-escape-sequences-are-deprecated/)

这个 JavaScript 异常 **0 前缀的八进制文字和八进制转义序列被弃用**仅在严格模式下工作。对于八进制文字，可以使用“0o”前缀。

**消息:**T0】

**错误类型:**

```
SyntaxError(in strict mode only)

```

**错误原因:**八进制文字和八进制转义序列被弃用，它们将在严格模式下抛出一个**语法错误****。语法不是 0o 就是 0O。**

****示例 1:** 这个示例使用了“0”前缀的八进制文字和八进制转义序列，因此出现了错误。**

 **## HTML

```
<script> 
   'use strict';
    var a = 04; // error here
</script>
```** 

****输出:****

```
SyntaxError: Octal numeric literals and escape characters not allowed in strict mode 
```

****示例 2:** 在本例中，使用了“0”前缀的八进制文字和八进制转义序列，因此出现了错误。**

 **## HTML

```
<script> 
   "use strict";
   var a = "\251"; // error here
</script>
```** 

****输出:****

```
SyntaxError: Octal numeric literals and escape characters not allowed in strict mode 
```