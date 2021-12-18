# JavaScript string . from codepoint()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-from code point/](https://www.geeksforgeeks.org/javascript-string-fromcodepoint/)

下面是 String.fromCodePoint()方法的示例。

*   **例:**

## java 描述语言

```
<script>
    a = String.fromCodePoint(71, 70, 71);
    document.write(a);
</script>
```

*   **输出:**

```
GFG
```

**String.fromCodePoint()** 是 JavaScript 中的一个内置方法，用于返回给定代码点值序列(ASCII 值)的字符串或元素。
[不同元素的码点值列表:](https://en.wikipedia.org/wiki/List_of_Unicode_characters)
**语法:**

```
String.fromCodePoint(a1, a2, a3, ....)
```

**参数:**这里参数 a1、a2 等是码点值的序列。
**返回值:**返回给定代码点值序列的对应字符串或元素。
显示 String.fromCodePoint()工作方式的 JavaScript 代码方法:
**代码#1:**

## java 描述语言

```
<script>

    // Taking some code point values
    a = String.fromCodePoint(42);
    b = String.fromCodePoint(65, 90);
    c = String.fromCodePoint(66, 65, 102);

    // Printing the corresponding elements of
    // the code point value.
    document.write(a + "<br>")
    document.write(b + "<br>")
    document.write(c + "<br>")

</script>
```

**输出:**

```
*
AZ
BAf
```

**代码#2:**

## java 描述语言

```
<script>
    // Taking some code point values
    a = String.fromCodePoint(71,101,101,107,115);

    // Printing the corresponding elements of
    // the code point value.
    document.write(a + "<br>")
</script>
```

**输出:**

```
Geeks
```

**支持的浏览器:**

*   Chrome 41 及以上
*   边缘 12 及以上
*   Firefox 29 及以上版本
*   歌剧 28 及以上
*   Safari 10 及以上