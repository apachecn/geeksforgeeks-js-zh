# 类型脚本|字符串子串()方法

> 原文:[https://www . geesforgeks . org/typescript-string-substring-method/](https://www.geeksforgeeks.org/typescript-string-substring-method/)

**子字符串()**是 [**类型脚本**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的一个内置函数，用于返回字符串对象的子集。

**语法:**

```
string.substring(indexA, [indexB]) 
```

**参数:**该方法接受如上所述的两个参数:

*   **indexA :** 此参数是 0 到比字符串长度小一的整数。
*   **indexB :** 该参数是 0 到字符串长度之间的整数。

**返回值:**该方法返回字符串对象的子集。
以下示例说明了 TypeScript 中的**字符串 substring()** 方法。

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String substring() Method
    var newstr = str.substring(0,5) 

    console.log(newstr);
</script>
```

**输出:**

```
Geeks

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String substring() Method
    var newstr = str.substring(0,5) 
    console.log(newstr);

    newstr = str.substring(-2,5) 
    console.log(newstr);

    newstr = str.substring(12,22) 
    console.log(newstr);

    newstr = str.substring(0,1) 
    console.log(newstr);
</script>
```

**输出:**

```
Geeks
Geeks
s - Best P
G

```