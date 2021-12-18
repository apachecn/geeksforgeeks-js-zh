# JavaScript isNaN()函数

> 原文:[https://www.geeksforgeeks.org/javascript-isnan-function/](https://www.geeksforgeeks.org/javascript-isnan-function/)

**isNaN()功能**用于检查给定值是否为非法数。如果值为 NaN，则返回 true，否则返回 false。它不同于 Number.isNaN()方法。

**语法:**

```
isNaN( value )
```

**参数值:**该方法接受上述单个参数，描述如下:

*   **值:**是在 isNaN()函数中传递的必需值。

**返回值:**它返回一个布尔值，即如果值为 NaN 则返回真，否则返回假。

## java 描述语言

```
<script>
    document.write(isNaN(12) + "<br>");
    document.write(isNaN(0 / 0) + "<br>");
    document.write(isNaN(12.3) + "<br>");
    document.write(isNaN("Geeks") + "<br>");
    document.write(isNaN("13/12/2020") + "<br>");
    document.write(isNaN(-46) + "<br>");
    document.write(isNaN(NaN) + "<br>");
</script>
```

**输出:**

```
false
true
false
true
true
false
true
```

**支持的浏览器:**

*   Chrome 1 及以上
*   Firefox 1 及以上版本
*   边缘 12 及以上
*   歌剧 3 及以上
*   Safari 1 及以上