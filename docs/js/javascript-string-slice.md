# JavaScript string.slice()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-slice/](https://www.geeksforgeeks.org/javascript-string-slice/)

下面是 string.slice()方法的示例。

*   **例:**

## java 描述语言

```
<script>                    
    var A = 'Geeks for Geeks';

    b = A.slice(0,5);
    c = A.slice(6,9);
    d = A.slice(10);

    document.write(b +"<br>");
    document.write(c +"<br>");
    document.write(d +"<br>");

</script>
```

*   **输出:**

```
Geeks
for
Geeks
```

**string.slice()** 是 javascript 中的一个内置方法，用于返回给定输入字符串的一部分或切片。
**语法:**

```
string.slice(startingindex, endingindex)
```

**参数:**该方法使用双参数 startingindex(从哪个索引开始，字符串就应该开始)和 endingindex(在哪个索引之前，应该包含字符串)。
**返回值:**返回给定输入字符串的一部分或一部分。
显示 string.slice()工作方式的 JavaScript 代码:
**代码#1:**

## java 描述语言

```
<script>                   

   // Taking a string as input.
   var A = 'Ram is going to school';

   // Calling of slice() function.
   b = A.slice(0, 5);

   // Here starting index is 1 given
   // and ending index is not given to it so
   // it takes to the end of the string 
   c = A.slice(1);

   // Here endingindex is -1 i.e, second last character
   // of the given string.
   d = A.slice(3, -1);
   e = A.slice(6);
   document.write(b +"<br>");
   document.write(c +"<br>");
   document.write(d +"<br>");
   document.write(e);   

</script>
```

**输出:**

```
Ram i
am is going to school
is going to schoo
going to school
```

**代码#2:**

## java 描述语言

```
<script>   
    // Taking a string as input.
    var A = 'Geeks for Geeks';

    // Calling of slice() function.
    // Here starting index is -1 given
    b = A.slice(-1,5);
    // Here endingindex is -1 i.e
    c = A.slice(0,-1);

    document.write(b +"<br>");
    document.write(c +"<br>");

</script>
```

**输出:**

```
Geeks for Geek
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   safari 1 及以上