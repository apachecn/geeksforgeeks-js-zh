# 类型脚本|字符串最后索引()方法

> 原文:[https://www . geesforgeks . org/typescript-string-last indexof-method/](https://www.geeksforgeeks.org/typescript-string-lastindexof-method/)

**lastIndexOf()** 是 TypeScript 中的一个内置函数，用于获取调用字符串对象中指定值最后一次出现的索引。
**语法:**

```
string.lastIndexOf(searchValue[, fromIndex]) 

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **搜索值:**此参数是一个字符串，表示要搜索的值。
*   **fromIndex:** 此参数是调用字符串中开始搜索的位置。

**返回值:**这个方法返回最后一次出现的索引，如果没有找到则返回-1。

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('TypeScript | \
    String lastIndexOf() Method with example'); 

    // use of String lastIndexOf() Method
    console.log(str1.lastIndexOf("String"));
</script>
```

**输出:**

```
17

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('TypeScript | \
    String lastIndexOf() Method with example'); 

    // use of String lastIndexOf() Method
    console.log(str1.lastIndexOf("Geeks"));
</script>
```

**输出:**

```
-1

```