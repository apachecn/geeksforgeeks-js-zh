# JavaScript string.normalize()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-normalize/](https://www.geeksforgeeks.org/javascript-string-normalize/)

下面是 string.normalize()方法的示例。

*   **例:**

## java 描述语言

```
<script>
var a = "Geeks For Geeks";

b = a.normalize('NFC')
c = a.normalize('NFD')
d = a.normalize('NFKC')
e = a.normalize('NFKD')

document.write(b,c,d,e);
</script>
```

*   **输出:**

```
Geeks For GeeksGeeks For GeeksGeeks For GeeksGeeks For Geeks
```

**string.normalize()** 是 javascript 中的一个内置方法，用于返回给定输入字符串的 Unicode 规范化形式。如果给定的输入不是字符串，那么首先它将被转换成字符串，然后这个方法将工作。
**语法:**

```
string.normalize([form])
```

**参数:**这里的参数是多种类型的形式-

*   NFC:规范化形式规范合成。
*   NFD:规范化形式典型分解。
*   NFKC:标准化表格兼容性组合。
*   NFKD:规范化表单兼容性分解。

这些都说 Unicode 规范化形式。
**返回值:**返回一个包含给定输入字符串的 Unicode 规范化形式的新字符串。
显示 string.normalize()工作方式的 JavaScript 代码方法:

## java 描述语言

```
<script>

  // Taking a string as input.
  var a = "GeeksForGeeks";

  // calling normalize method.
  b = a.normalize('NFC')
  c = a.normalize('NFD')
  d = a.normalize('NFKC')
  e = a.normalize('NFKD')

  // Printing normalised form.
  document.write(b +"<br>");
  document.write(c +"<br>");
  document.write(d +"<br>");
  document.write(e);

</script>
```

**输出:**

```
GeeksForGeeks
GeeksForGeeks
GeeksForGeeks
GeeksForGeeks
```

**支持的浏览器:**

*   谷歌 Chrome 34 及以上
*   边缘 12 及以上
*   Firefox 31 及以上版本
*   歌剧 21 及以上
*   Safari 10 及以上