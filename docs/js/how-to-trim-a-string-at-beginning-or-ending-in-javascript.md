# 如何在 JavaScript 中修剪字符串的开头或结尾？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中开始或结束时修剪字符串/](https://www.geeksforgeeks.org/how-to-trim-a-string-at-beginning-or-ending-in-javascript/)

本文演示了如何在开始、结束以及两边修剪字符串。对于各种各样的字符串修剪，JavaScript 提供了三个功能。 [TrimLeft()](https://www.geeksforgeeks.org/javascript-trimstart-and-trimleft-method/) ，用于删除字符串开头的字符。 [TrimRight()](https://www.geeksforgeeks.org/javascript-trimend-and-trimright-method/) ，用于删除字符串末尾的字符。 [Trim()](https://www.geeksforgeeks.org/javascript-string-prototype-trim-function/) ，用于去除两端字符。与许多其他语言一样，JavaScript 的本机函数只移除空白字符。我们将详细讨论所有这些功能，&通过示例了解它们。

**在开始处修剪字符串:**在这种情况下，我们使用 *trimLeft()* 函数在开始处修剪字符串。

[**【JavaScript trimLeft()】函数:**](https://www.geeksforgeeks.org/javascript-trimstart-and-trimleft-method/) 此方法用于消除字符串开头的空格。字符串的值不会以任何方式改变，如果字符串后面有任何空格，它不会被修改。

**语法:**

```
string.trimLeft();
```

**示例 1:** 在本例中，变量 var 用字符串“geeksforgeeks”声明。请注意，给定的字符串在左端有空白。函数的作用是:删除开头的空白。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Javascript trimLeft() Function</title>
</head>

<body>
    <script>
    var word = " geeksforgeeks";
    console.log("initial string:" + "'" + word + "'");

    // Trimming the string at the Beginning 
    var new_word = word.trimLeft();
    console.log("modified string:" + "'" + new_word + "'");
    </script>
</body>

</html>
```

**输出**:

```
initial string:' geeksforgeeks'
modified string:'geeksforgeeks'
```

**示例 2** :在本例中，变量 var 用字符串“geeksforgeeks”声明。请注意，给定的字符串两端都有空白。trimLeft()将只删除开头的空白，而保持结尾的空白不变。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Javascript trimLeft() Function</title>
</head>

<body>
    <script>
    var word = " geeksforgeeks ";
    console.log("initial string:" + "'" + word + "'");

    // Trimming the string at the start
    var new_word = word.trimLeft();
    console.log("modified string:" + "'" + new_word + "'");
    </script>
</body>

</html>
```

**输出:**

```
initial string:' geeksforgeeks '
modified string:'geeksforgeeks '
```

**修剪末端的字符串:**在这种情况下，我们使用 trimRight()函数修剪末端的字符串。

[**JavaScript trimRight()函数** :](https://www.geeksforgeeks.org/javascript-trimend-and-trimright-method/) 这个方法是用来消除字符串末尾的空格。字符串的值不会以任何方式改变，如果字符串前面有任何空格，它不会被修改。

**语法:**

```
string.trimRight();
```

**示例 1:** 在此示例中，声明了一个变量 var，并为其赋予了字符串“geeksforgeeks”。请注意，给定的字符串在右端有空白，因此 trimRight()会删除末尾的空白。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Javascript trimRight() Function</title>
</head>

<body>
    <script>
    var word = "geeksforgeeks ";
    console.log("initial string:" + "'" + word + "'");

    // Trimming the string at the right end
    var new_word = word.trimRight();
    console.log("modified string:" + "'" + new_word + "'");
    </script>
</body>

</html>
```

**输出:**

```
initial string:'geeksforgeeks '
modified string:'geeksforgeeks'
```

**示例 2:** 在此示例中，声明了一个变量 var，并为其赋予了字符串“geeksforgeeks”。请注意，给定的字符串两端都有空白。函数的作用是:删除末尾的空格，而不是开头的空格。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Javascript trimRight() Function</title>
</head>

<body>
    <script>
    var word = " geeksforgeeks ";
    console.log("initial string:" + "'" + word + "'");

    // Trimming the string at the right end
    var new_word = word.trimRight();
    console.log("modified string:" + "'" + new_word + "'");
    </script>
</body>

</html>
```

**输出:**

```
initial string:' geeksforgeeks '
modified string:' geeksforgeeks'
```

**从两端修剪字符串:**在这种情况下，我们使用 trim()函数在两端修剪字符串。

[**JavaScript trim()函数:**](https://www.geeksforgeeks.org/javascript-string-prototype-trim-function/) Trim()消除字符串两端的空白，生成一个新的字符串，而不改变原来的字符串。在此上下文中，所有空白字符和所有行结束符都被视为空白。

**语法:**

```
string.trim();
```

**示例:**在此示例中，声明了一个变量 var，并为其赋予了字符串“geeksforgeeks”。请注意，给定的字符串两端都有空白。trim()删除两端的空白。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Javascript trim() Function</title>
</head>

<body>
    <script>
    var word = " geeksforgeeks ";
    console.log("initial string:" + "'" + word + "'");

    // Trimming the string at both ends
    var new_word = word.trim();
    console.log("modified string:" + "'" + new_word + "'");
    </script>
</body>

</html>
```

**输出:**

```
initial string:' geeksforgeeks '
modified string:'geeksforgeeks'
```

**支持的浏览器:**

*   谷歌 Chrome 4.0
*   Firefox 3.5
*   Internet Explorer 10.0
*   微软边缘 12.0
*   歌剧 10.5
*   Safari 5.0