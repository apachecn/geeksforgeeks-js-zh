# 类型脚本|字符串子字符串()方法

> 原文:[https://www . geesforgeks . org/typescript-string-substr-method/](https://www.geeksforgeeks.org/typescript-string-substr-method/)

**split()** 是 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的一个内置函数，用于通过指定的字符数返回从指定位置开始的字符串中的字符。

**语法:**

```
string.substr(start[, length])
```

**参数:**该方法接受两个参数，如上所述，如下所述。：

*   **开始**–该参数是开始提取字符的位置。
*   **长度**–该参数是要提取的字符数。

**返回值:**该方法返回新的子字符串。
以下示例说明了 TypeScript 中的**字符串 substr()** 方法。

**例 1:**

## java 描述语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String substr() Method
    var newstr = str.substr(0,5) 

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

    // use of String substr() Method
    var newstr = str.substr(0,5) 
    console.log(newstr);

    newstr = str.substr(-2,5) 
    console.log(newstr);

    newstr = str.substr(12,22) 
    console.log(newstr);

    newstr = str.substr(0,1) 
    console.log(newstr);
</script>
```

**输出:**

```
Geeks
rm
s - Best Platform
G

```