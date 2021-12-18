# JavaScript string.repeat()方法

> 原文:[https://www.geeksforgeeks.org/javascript-string-repeat/](https://www.geeksforgeeks.org/javascript-string-repeat/)

下面是 string.repeat()方法的示例。

*   **Example:**

## Javascript

```
<script>
    A = "forGeeks";
    a = A.repeat(2);
    document.write(a);
</script>
```

**输出:**

```
forGeeksforGeeks
```

**string.repeat()** 是 JavaScript 中的一个内置函数，用于构建一个新的字符串，该字符串包含调用该函数的字符串的指定数量的副本。

**语法:**

```
string.repeat(count);
```

*   **计数:** *计数*是一个整数值，表示重复给定字符串的次数。整数“计数”的范围从零(0)到无穷大。

**返回值:**它返回一个新字符串，该字符串包含指定数量的字符串副本。

**显示 string.repeat()函数工作原理的 JavaScript 代码:**

**代码# 1:**

## JavaScript

```
<script>

    // Taking a string "gfg"
    A = "gfg";

    // Repeating the string multiple times
    a = A.repeat(5);
    document.write(a);

</script>
```

**输出:**

```
gfggfggfggfggfg
```

**代码# 2:**

## JavaScript

```
<script>

    // Taking a string "gfg"
    A = "gfg";

    // Repeating the string 2.9 times i.e, 2 times
    // because 2.9 converted into 2
    b = A.repeat(2.9);
    document.write(b + "<br>");

</script>
```

**输出:**

```
gfggfg
```

**支持的浏览器:**

*   Google Chrome 41 and above
*   Edge 12 and above
*   Firefox 24 and above
*   Opera 28 and above
*   Safari 9 and above