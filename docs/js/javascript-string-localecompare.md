# JavaScript string . locale compare()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-locale compare/](https://www.geeksforgeeks.org/javascript-string-localecompare/)

下面是字符串. localeCompare()方法的示例。

*   **例:**

    ```
    <script>
        gfg = 'b'.localeCompare('a'); 
        document.write(gfg + '<br>') 
    </script>
    ```

*   **输出:**

    ```
    1
    ```

**string.localeCompare()** 是 JavaScript 中的一个内置方法，用于比较任意两个元素，如果引用字符串在字典序上大于比较字符串，则返回正数，如果引用字符串在字典序上小于比较字符串，则返回负数，如果比较字符串和引用字符串相等，则返回零(0)。
**语法:**

```
referenceString.localeCompare(compareString)
```

**参数:**这里的参数 compareString 是一个与引用字符串进行比较的字符串。
**返回值:**如果引用字符串在字典序上大于比较字符串，则返回正数；如果引用字符串在字典序上小于比较字符串，则返回负数；如果比较字符串和引用字符串相等，则返回零(0)。

显示 string.localeCompare()方法工作原理的 JavaScript 代码:
**代码#1:**

```
<script>

    // An alphabet "n" comes before "z" which
    // gives a negative value
    a = 'n'.localeCompare('z');
    document.write(a + '<br>')

    // Alphabetically the word "gfg" comes after
    // "geeksforgeeks" which gives a positive value
    b = 'gfg'.localeCompare('geeksforgeeks');
    document.write(b + '<br>')

    // "gfg" and "gfg" are equivalent which
    // gives a value of zero(0)
    c = 'a'.localeCompare('a');
    document.write(c)

</script>
```

**输出:**

```
-1
1
0
```

**代码#2:** 这个方法也用于元素排序。

```
<script>

    // Taking some elements to sort alphabetically
    var elements = [ 'gfg', 'geeksforgeeks', 'cse', 'department' ];
    a = elements.sort((a, b) => a.localeCompare(b));

    // Returning sorted elements
    document.write(a)

</script>
```

**输出:**

```
cse, department, geeksforgeeks, gfg
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 7 及以上
*   Safari 3 及以上版本