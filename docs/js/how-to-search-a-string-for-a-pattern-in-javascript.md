# 如何在 JavaScript 中搜索字符串寻找模式？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中搜索字符串模式/](https://www.geeksforgeeks.org/how-to-search-a-string-for-a-pattern-in-javascript/)

在本文中，我们将看到如何在 JavaScript 中搜索字符串模式。我们将使用以下方法来搜索字符串:

**方法 1:** 在这里，我们将学习如何在 JavaScript 中搜索包含给定模式的字符串。 [string.search()](https://www.geeksforgeeks.org/javascript-string-search/) 方法是 JavaScript 中用于此目的的内置方法。它搜索给定字符串中正则表达式之间的匹配。

**语法:**

```
let position = str.search( expression )
```

**参数:**string . search()方法接受两个参数:

*   **字符串名称:**我们要在其中搜索模式的字符串的名称作为参数。
*   **表达式:**是我们要检查的模式/子串是否存在于上述字符串中。

**返回值:**返回给定字符串中第一个匹配正则表达式的索引值，否则返回-1。它从索引 0 开始，如果匹配了任何字母表，它将返回其对应的索引，并且不再进一步检查。

**例 1:**

## JavaScript

```
<script>

    // Taking input a string.
    var string = "GeeksforGeeks is computer science portal";

    // Taking a regular expression.
    var regexp1 = /G/;  
    var regexp2 = /c/;
    var regexp3 = /z/;

    // Output
    console.log(string.search(regexp1));
    //Expected Output: 0

    console.log(string.search(regexp2));
    // Expected Output: 17

    console.log(string.search(regexp3));
    // Expected Output: -1
</script>
```

**输出:**

```
0
17
-1
```

**解释:**我们可以观察到第一个“ **G** ”匹配出现在索引 0，而第一个“ **c** ”匹配出现在第 17 个索引，而字母“ **z** ”在字符串“GeeksforGeeks 是计算机科学门户”中不存在，因此返回-1。

**例二:**

## JavaScript

```
<script>

    // Taking input a string.
    var string = "GeeksforGeeks is computer science portal";

    // Taking a regular expression.
    var regexp = /cie/;  

    console.log(string.search(regexp));
    // Expected Output: 27
</script>
```

**输出:**

```
27
```

**解释:**我们可以观察到表达式‘CIE’与索引 27 处的 String 匹配。因此，如果正则表达式的第一个匹配元素存在于给定的字符串中，它将返回该元素的索引。

**方法 2:** 我们还可以使用 [Javascript String match()](https://www.geeksforgeeks.org/javascript-match-function/) 函数，只要找到与给定字符串匹配的字符串，该函数就会返回包含给定表达式的数组，否则返回 null。

**语法:**

```
string.match( expression )
```

**参数:**这里取两个参数:

*   **String name:** We want the name of the string of the search pattern as a parameter.
*   **Expression** : It is whether the pattern/substring we want to check exists in the above string.

**例 1:**

## JavaScript

```
<script>

    // Taking input a string.
    let string = "GeeksforGeeks is computer science portal";
    console.log(string.match(/rGe/g));    
</script>
```

**输出:**

```
['rGe']
0: "rGe"
length: 1
[[Prototype]]: Array(0)
```

因此，它返回一个长度为 1 的数组，因为给定表达式和字符串之间只有一个匹配项。“g”标志有助于在给定的字符串和表达式之间找到区分大小写的匹配。

对于全局的、不区分大小写的匹配，我们可以使用“gi”标志，它将返回给定字符串的所有可能组合。

**例二:**

## JavaScript

```
<script>

    // Taking input a string.
    let string = "GeeksforGeeks is computer "
        + "science portal for computer geeks";
        console.log(string.match(/gee/gi));
</script>
```

**输出:**

```
['Gee', 'Gee', 'gee']
0: "Gee"
1: "Gee"
2: "gee"
length: 3
[[Prototype]]: Array(0)
```

因此，它返回一个长度为三的数组，该数组包含给定表达式/模式和字符串之间的所有可能组合。