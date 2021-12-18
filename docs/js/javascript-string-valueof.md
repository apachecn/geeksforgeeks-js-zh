# JavaScript string.valueOf()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-string-value of/

下面是 string.valueOf()方法的示例。

*   **例:**

## java 描述语言

```
<script>
    var a = new String("GeeksforGeeks");
    document.write(a.valueOf());
</script>
```

*   **输出:**

```
GeeksforGeeks
```

**字符串. valueOf()** 是 JavaScript 中的一个内置方法，用于返回给定字符串的值。
**语法:**

```
string.valueOf()
```

**参数:**不接受任何参数。
**返回值:**返回一个代表给定字符串对象值的字符串。
**显示 string.valueOf()工作方式的 JavaScript 代码:**
**程序 1:**

## java 描述语言

```
<script>
    // Taking a string as input and printing it
    // with the help of string.valueOf() function
    var a = new String("GeeksforGeeks");
    document.write(a.valueOf());
</script>
```

**输出:**

```
GeeksforGeeks
```

**节目 2:**

## java 描述语言

```
<script>
    // Taking a string as input and printing it
    // with the help of string.valueOf() function
    var a = new String("Geeks");
    var b = new String("for");
    var c = new String("Geeks");
    document.write(a.valueOf(),b.valueOf(),c.valueOf());
</script>
```

**输出:**

```
GeeksforGeeks
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上