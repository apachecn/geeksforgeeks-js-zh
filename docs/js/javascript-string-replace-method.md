# JavaScript string.replace()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-replace-method/](https://www.geeksforgeeks.org/javascript-string-replace-method/)

下面是字符串替换()方法的示例。

*   **例:**

## java 描述语言

```
<script>
    var string = 'GeeksForGeeks';
    var newstring = string.replace(/GeeksForGeeks/, 'GfG');

    document.write(newstring);
</script>
```

*   **输出:**

```
GfG
```

**string.replace()** 是 JavaScript 中的一个内置方法，用于用另一个字符串或正则表达式替换给定字符串的一部分。原始字符串将保持不变。
**语法:**

```
str.replace(A, B)
```

**参数:**这里的参数 A 是正则表达式，B 是将替换给定字符串内容的字符串。
**返回值:**返回一个有替换项的新字符串。
**JavaScript 代码展示了这个方法的工作原理:**
**代码#1:**
这里字符串 GeeksForGeeks 的内容将被替换为 gfg。

## java 描述语言

```
<script>

    // Assigning a string
    var string = 'GeeksForGeeks is a CS portal';

// Calling replace() method
var newstring = string.replace(/GeeksForGeeks/, 'gfg');

// Printing replaced string
document.write(newstring);

</script>
```

**输出:**

```
gfg is a CS portal
```

**代码#2:**

## java 描述语言

```
<script>

    // Taking a regular expression
    var re = /GeeksForGeeks/;

// Taking a string as input
var string = 'GeeksForGeeks is a CS portal';

// Calling replace() method to replace
// GeeksForGeeks from string with gfg
var newstring = string.replace(re, 'gfg');

// Printing new string with replaced items
document.write(newstring);

</script>
```

**输出:**

```
gfg is a CS portal
```

**支持的浏览器:**

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上