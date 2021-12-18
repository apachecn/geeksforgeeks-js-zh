# 类型脚本|字符串值 Of()方法

> 原文:[https://www . geesforgeks . org/typescript-string-value of-method/](https://www.geeksforgeeks.org/typescript-string-valueof-method/)

**valueOf()** 是 [**类型脚本**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的一个内置函数，用于返回字符串对象的原始值。

**语法:**

```
string.valueOf( ) 
```

**参数:**此方法不接受任何参数。
**返回值:**这个方法返回一个 String 对象的原始值。
以下示例说明了 TypeScript 中的**字符串值()**方法

**例 1:**

## Java Script 语言

```
//language is TypeScript

    // Original strings
    var str = "Geeksforgeeks - Best Platform";

    // use of String valueOf() Method
    var newstr = str.valueOf()
    console.log(newstr);
```

**输出:**

```
Geeksforgeeks - Best Platform
```

**例 2:**

## Java Script 语言

```
// Language is TypeScript

    // Original strings
    var str = new String("TypeScript - String valueOf()");

    // use of String valueOf() Method
    var newstr = str.valueOf()
    console.log(newstr);
```

**输出:**

```
TypeScript - String valueOf()
```