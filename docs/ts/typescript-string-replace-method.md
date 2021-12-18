# 类型脚本|字符串替换()方法

> 原文:[https://www . geesforgeks . org/typescript-string-replace-method/](https://www.geeksforgeeks.org/typescript-string-replace-method/)

**replace()** 是 TypeScript 中的一个内置函数，用于查找正则表达式和字符串之间的匹配，并用新的子字符串替换匹配的子字符串。
**语法:**

```
string.replace(regexp/substr, newSubStr/function[, flags]);
```

**参数:**该方法接受如上所述和下述五个参数:

*   **regexp:** 这个参数是一个 regexp 对象。
*   **子字符串:**此参数是要替换的字符串。
*   **新子字符串:**此参数是替换子字符串的字符串。
*   **函数:**该参数是一个用来创建新子串的函数。
*   **标志:**该参数是一个包含任意组合的正则表达式标志的字符串。

**返回值:**该方法返回一个新的已更改的字符串。

下面的示例说明了 TypeScriptJS 中的**字符串替换()**方法:

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Good Platform"; 

    var re = /Good/gi; 

    // Use of String replace() Method
    var newstr = str.replace(re, "Best"); 
    console.log(newstr);
</script>
```

**输出:**

```
Geeksforgeeks - Best Platform

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks TypeScript"; 

    var re = /(\w+)\s(\w+)/; 

    // use of String replace() Method
    var newstr = str.replace(re, "$2 $1"); 
    console.log(newstr);
</script>
```

**输出:**

```
TypeScript Geeksforgeeks

```