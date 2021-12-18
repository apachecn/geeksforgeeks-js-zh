# JavaScript 字符串修剪()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-trim-function/](https://www.geeksforgeeks.org/javascript-string-prototype-trim-function/)

下面是字符串修剪()方法的示例。

*   **示例:**

## Java Script 语言

```
<script>
function func() {
    var str = "GeeksforGeeks      ";
    var st = str.trim();
    document.write(st);
}
func();
</script>
```

*   输出:

```
GeeksForGeeks
```

**str.trim()** 方法用于删除给定字符串两端的空格。

**语法:**

```
str.trim()
```

**返回值:**
这个方法返回一个新的字符串，没有任何前导或尾随空格。

*<u>上述方法示例如下:</u>*

**例 1:**

```
var str = "GeeksforGeeks      ";
var st = str.trim();
print(st);
```

输出:

```
GeeksForGeeks
```

在本例中， **trim()** 方法删除字符串**字符串**中的所有前导和尾随空格。

**例 2:**

```
var str = "   GeeksforGeeks";
var st = str.trim();
print(st);
```

输出:

```
GeeksForGeeks
```

在本例中， **trim()** 方法删除字符串**字符串**中的所有前导和尾随空格。

*<u>上述方法的代码如下:</u>*

**程序 1:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate trim() method

function func() {

    // Original string containing whitespace
    var str = "GeeksforGeeks      ";

    // Trimmed string
    var st = str.trim();
    document.write(st);
}

func();
</script>
```