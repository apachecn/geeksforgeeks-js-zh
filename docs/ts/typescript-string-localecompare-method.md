# 类型脚本|字符串 localeCompare()方法

> 原文:[https://www . geesforgeks . org/typescript-string-locale compare-method/](https://www.geeksforgeeks.org/typescript-string-localecompare-method/)

**localeCompare()** 是 TypeScript 中的一个内置函数，用于获取数字，该数字指示引用字符串是在给定字符串之前还是之后，还是与给定字符串在排序顺序上相同。
**语法:**

```
string.localeCompare( param ) 

```

**参数:**该方法接受如上所述的单个参数。

*   **参数:**此参数是要与字符串对象进行比较的字符串。

**返回值:**此方法返回流水。

*   **0** 是返回，如果字符串完全匹配。
*   **1** 是返回，如果字符串不匹配并且参数值在字符串对象的值之前。
*   –如果字符串不匹配，并且参数值在字符串对象的值之后，则返回值为负值。

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('Geeksforgeeks'); 

    var index = str1.localeCompare("Geeksforgeeks");

    // Use of String localeCompare() Method
    console.log(index);
</script>
```

**输出:**

```
0

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('Geeksforgeeks'); 

    var index = str1.localeCompare("Geeks");

    // Use of String localeCompare() Method
    console.log(index);
</script>
```

**输出:**

```
1

```