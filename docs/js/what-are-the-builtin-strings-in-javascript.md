# JavaScript 中有哪些内置字符串？

> 原文:[https://www . geesforgeks . org/什么是内置 javascript 字符串/](https://www.geeksforgeeks.org/what-are-the-builtin-strings-in-javascript/)

一系列字母、特殊字符、数字等。或者它们的组合被称为*弦*。字符串是通过将字符串包含在单引号(')或双引号(")中来创建的。

**语法:**

```
var myString = 'Good Morning123!'; // Single quoted string
var myString = "Good Morning123!"; // Double quoted string
```

在 Javascript 中，许多字符串方法要么是内置的，要么是用户定义的。*内置*字符串方法是存在于任何*编程语言库中*的方法。

**JavaScript 的内置字符串方法:**

*   **search():** 用于在字符串中搜索特定的值或表达式。它返回匹配的位置。
*   **split():** 用于将一个字符串拆分为一个子字符串数组。
*   **startsWith():** 用于检查字符串是否以指定字符开头。
*   **slice():** 用于提取字符串的一部分并返回新的字符串。
*   **concat():** 用于合并两个字符串的文本，返回一个新的字符串。
*   **charAt():** 用于返回指定索引处的字符。
*   **indexOf()** 用于返回字符串对象中指定值的索引，该索引首先出现。如果找不到对象，则返回-1。
*   **lastIndexOf():** 用于返回字符串对象中最后出现的指定值的索引。如果找不到对象，则返回-1。
*   **match():** 用于匹配正则表达式和字符串。
*   **replace():** 用于查找正则表达式与字符串的匹配。匹配的子字符串被新的子字符串替换。
*   **substr():** 用于从指定位置开始，通过指定的字符数返回字符串中的字符。
*   **substring():** 用于返回两个指定索引之间的字符串中的字符。
*   **toLowerCase():** 用于将调用的字符串值转换为小写。
*   **toUpperCase():** 用于将调用的字符串值转换为大写。
*   **valueOf():** It is used to return the primitive value of the specified object.

    **用户定义的字符串方法:**由用户定义的执行特定任务的方法*。*

*   **JavaScript 中用户定义的字符串方法:**
    *   **logIt():** 用于在执行代码时，将一个参数记录回控制台。
    *   **return():** 用于明确返回特定值。

**例:** Search()方法。

```
<p id="demo"></p>

function myFunction() {
  var str = "Welcome to GeeksforGeeks!"; 
  var a= str.search("GeeksforGeeks");
  document.getElementById("demo").innerHTML = a;
}
```

**输出:**

```
11
```

**例:** split()方法。

```
<p id="demo"></p>

function myFunction() {
  var str = "How are you feeling today?";
  var res = str.split(" ");
  document.getElementById("demo").innerHTML = res;
}
```

<strng>输出:</strng>

```
How, are, you, feeling, today?
```

**例:**用()方法启动。

```
<p id="demo"></p>

function myFunction() {
  var str = "Hello world, welcome to the universe.";
  var n = str.startsWith("Hello");
  document.getElementById("demo").innerHTML = n;
}
```

**输出:**

```
true
```