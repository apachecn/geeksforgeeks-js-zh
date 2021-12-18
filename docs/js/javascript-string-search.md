# JavaScript string.search()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-search/](https://www.geeksforgeeks.org/javascript-string-search/)

**string.search()方法**是 JavaScript 中的内置方法，用于搜索[正则表达式](https://www.geeksforgeeks.org/javascript-regular-expressions/)和给定字符串对象之间的匹配。

**语法:**

```
string.search( A )
```

**参数:**该方法接受单个参数 **A** ，该参数将正则表达式作为对象。

**返回值:**此函数返回正则表达式和给定字符串对象之间的第一个匹配字符串的索引，如果没有找到匹配项，则返回-1。索引从零(0)开始，在第一次尝试中，一个字母表被匹配，然后它不再进一步检查。简单地说，它返回第一个匹配字母表的索引。

**示例 1:** 下面的示例说明了 JavaScript 中的 **string.search()** 方法。

## java 描述语言

```
<script>

  // Taking input a string.
  var string = "GeeksforGeeks";

  // Taking a regular expression.
  var re1 = /G/;
  var re2 = /e/;
  var re3 = /s/;

  // Printing the index of matching alphabets
  document.write(string.search(re1) + "<br>");
  document.write(string.search(re2) + "<br>");
  document.write(string.search(re3));
< /script>
```

**输出:**

```
0
1
4
```

**示例 2:** 此示例返回-1，因为在正则表达式和输入字符串之间找不到匹配。

## java 描述语言

```
<script>

  // Taking input a string.
  var string = "GeeksforGeeks";

  // Taking a regular expression.
  var re1 = /p/;
  var re2 = /1/;
  var re3 = / /;
  var re4 = /, /;

  // Printing the index of matching alphabets
  document.write(string.search(re1) + "<br>");
  document.write(string.search(re2) + "<br>");
  document.write(string.search(re3) + "<br>");
  document.write(string.search(re4));
< /script>
```

**输出:**

```
-1
-1
-1
-1
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上