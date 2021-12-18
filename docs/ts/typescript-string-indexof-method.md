# 类型脚本|字符串索引 Of()方法

> 原文:[https://www . geesforgeks . org/typescript-string-indexof-method/](https://www.geeksforgeeks.org/typescript-string-indexof-method/)

**indexOf()** 是 TypeScript 中的一个内置函数，用于获取指定值第一次出现时调用 String 对象中的索引。
**语法:**

```
string.indexOf(searchValue[, fromIndex]) 
```

**参数:**该方法接受两个参数，如上所述，如下所述。

*   **搜索值:**此参数是一个字符串，表示要搜索的值。
*   **fromIndex:** 此参数是调用字符串中开始搜索的位置。

**返回值:**该方法返回找到的匹配项的索引，否则，如果没有找到，返回-1。

以下示例说明了 TypeScriptJS 中的**字符串 indexOf()** 方法:
**示例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('TypeScript | \
String indexOf() Method with example'); 

    // use of String indexOf() Method
    console.log(str1.indexOf("String"));
</script>
```

**输出:**

```
13

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('TypeScript | \
    String indexOf() Method with example'); 

    // use of String indexOf() Method
    console.log(str1.indexOf("Geeks"));
</script>
```

**输出:**

```
-1

```