# JavaScript 字符串拆分()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-prototype-split-function/](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)

下面是字符串拆分()方法的示例。

*   **例:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate split() function

function func() {
    //Original string
    var str = 'Geeks for Geeks'
    var array = str.split("for");
    document.write(array);
}

func();
</script>
```

*   输出:

```
Geeks , Geeks
```

**str.split()** 方法用于使用参数中提供的指定分隔符将给定的字符串分成子字符串，从而将其拆分为字符串数组。
**语法:**

```
str.split(separator, limit)
```

*   **分隔符:**用于指定用于拆分字符串的字符或正则表达式。如果未指定**分隔符**，则整个字符串成为一个单个数组元素。当字符串中不存在**分隔符**时，也会发生同样的情况。如果**分隔符**是空字符串( **""** )，则字符串的每个字符都会被分隔。
*   **限制:**定义在给定字符串中找到的拆分数量的上限。如果字符串在达到**限制**后仍未被选中，则不会在数组中报告。

**返回值**
该函数返回一个字符串数组，该数组是在分隔符出现的每个点拆分给定字符串后形成的。
*<u>上述功能示例如下:</u>*
**示例 1:**

```
var str = 'It iS a 5r&e@@t Day.'
var array = str.split(" ");
print(array);
```

输出:

```
[It,iS,a,5r&e@@t,Day.]
```

在本例中，函数 **split()** 通过在出现**“**的任何地方拆分**字符串**来创建字符串数组。
**例 2:**

```
var str = 'It iS a 5r&e@@t Day.'
var array = str.split(" ",2);
print(array);
```

输出:

```
[It,iS]
```

在本例中，函数 **split()** 通过在出现**“**的任何地方拆分**字符串**来创建字符串数组。第二个参数 **2** 将这种拆分的数量限制为只有 2 个。
*<u>上述功能的代码如下:</u>*
**程序 1:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate split() function

function func() {
    //Original string
    var str = 'It iS a 5r&e@@t Day.'
    var array = str.split(" ");
    document.write(array); 
}

func();
</script>
```

输出:

```
[It,iS,a,5r&e@@t,Day.]
```

**节目 2:**

## Java Script 语言

```
<script>
// JavaScript Program to illustrate split() function

function func() {

    // Original string
    var str = 'It iS a 5r&e@@t Day.'

    // Splitting up to 2 terms
    var array = str.split(" ",2);
    document.write(array);
}

func();
</script>
```

输出:

```
[It,iS]
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。