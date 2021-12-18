# 类型脚本|字符串切片()方法示例

> 原文:[https://www . geesforgeks . org/typescript-string-slice-method-with-example/](https://www.geeksforgeeks.org/typescript-string-slice-method-with-example/)

**切片()**是 TypeScript 中的一个内置函数，用于提取字符串的一部分并返回一个新字符串。
**语法:**

```
string.slice( beginslice [, endSlice] )
```

**参数:**该方法接受如上所述和如下所述两个参数:

*   **开始提取**–该参数是从零开始提取的索引。
*   **结束切片**–该参数是结束提取的从零开始的索引。

**返回值:**这个方法返回字符串内部正则表达式的索引。否则，它返回-1。

下面的示例说明了 TypeScriptJS 中的**字符串切片()**方法:

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String slice() Method
    var newstr = str.slice(0,14); 

    console.log(newstr);
</script>
```

**输出:**

```
Geeksforgeeks

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String slice() Method
    var newstr = str.slice(16); 

    console.log(newstr);
</script>
```

**输出:**

```
Best Platform

```