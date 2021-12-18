# JavaScript 只保留字符串中的前 N 个字符

> 原文:[https://www . geesforgeks . org/JavaScript-to-keep-only-n-characters in-a-string/](https://www.geeksforgeeks.org/javascript-to-keep-only-first-n-characters-in-a-string/)

给定一个字符串，任务是只保留字符串的前 n 个字符。在 JavaScript 中有各种方法可以解决这个问题，下面讨论其中一些方法:

**方法 1:使用 [substring()方法](https://www.geeksforgeeks.org/javascript-string-substring/):**string . substring()方法是 JavaScript 中的一个内置函数，用于返回给定字符串从起始索引到结束索引的部分。索引从零(0)开始。

**语法:**

```
string.substring(Startindex, Endindex)
```

下面的程序演示了上述方法。

**示例:**

```
<script>
    // JavaScript to keep only first
    // 'n' characters of String

    // Original string
    var str = "GeeksforGeeks";

    // Keep first 5 letters
    var n = 5;

    document.write("Original String = \""
                    + str + "\"<br>");
    document.write("n = " + n + "<br>");

    // Using substring() method
    str = str.substring(0, n);

    document.write("Keep first " + n + 
        " characters of original String = \""
        + str + "\"<br>");
</script>                                     
```

**输出:**

```
Original String = "GeeksforGeeks"
n = 5
Keep first 5 characters of original String = "Geeks"

```

**方法 2:使用 [slice()方法](https://www.geeksforgeeks.org/javascript-string-slice/):**string . slice()是 javascript 中的一个内置函数，用于返回给定输入字符串的一部分或切片。

**语法:**

```
string.slice(startingindex, endingindex)
```

下面的程序演示了上述方法。

**示例:**

```
<script>
    // JavaScript script to keep only
    // first 'n' characters of String

    // Original string
    var str = "Data Structure";

    // Keep first 11 letters
    var n = 11;

    document.write("Original String = \""
                    + str + "\"<br>");
    document.write("n = " + n + "<br>");

    // Using slice() method
    str = str.slice(0, n);

    document.write("Keep first " + n + 
        " characters of original String = \""
        + str + "\"<br>");
</script>                    
```

**输出:**

```
Original String = "Data Structure"
n = 11
Keep first 11 characters of original String = "Data Struct"

```