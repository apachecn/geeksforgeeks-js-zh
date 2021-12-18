# 类型脚本|字符串字符()方法

> 原文:[https://www . geesforgeks . org/typescript-string-charat-method/](https://www.geeksforgeeks.org/typescript-string-charat-method/)

TypeScript 中的 **charAt()** **方法**用于返回字符串指定索引处的字符。字符串从左到右进行索引。

**语法:**

```
string.charAt( index )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **索引:**是小于字符串长度的 0 到 1 之间的整数值。

**返回值:**该方法返回参数中给定索引的一个字符。

以下示例说明了 **charAt()方法**在 TypeScript 中的工作:
**示例 1:**

## 以打字打的文件

```
// Original string
var str = new String(
    'JavaScript is object oriented language');

// Finding the character at given index 
var value = str.charAt(14);
console.log(value);
```

**输出:**

```
o
```

**例 2:**

## 以打字打的文件

```
// Original string
var str = new String(
    'JavaScript is object oriented language');

// Finding the character at given index 
console.log("str.charAt(0) is: " + str.charAt(0));
console.log("str.charAt(1) is: " + str.charAt(1)); 
```

**输出:**

```
str.charAt(0) is:J
str.charAt(1) is:a
```