# 类型脚本|字符串 concat()方法

> 原文:[https://www . geesforgeks . org/typescript-string-concat-method/](https://www.geeksforgeeks.org/typescript-string-concat-method/)

**concat()** 是 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的一个内置函数，用于添加两个或多个字符串并返回一个新的单个字符串。

**语法:**

```
string.concat(string2, string3[, ..., stringN]); 
```

**参数:**该方法接受如上所述和如下所述的单个参数。

*   **string 2…string:**此参数保存将要连接的字符串。

**返回值:**这个方法返回串联的字符串。

下面的示例说明了 TypeScriptJS 中的**字符串 concat()** 方法:

**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('GeeksforGeeks'); 
    var str2 = new String(' - Best Platform'); 

    // Combines the text of two strings and 
    // returns a new string.
    console.log("Concatenated String : " 
            + str1.concat(str2.toString()));
</script>
```

**输出:**

```
Concatenated String : GeeksforGeeks - Best Platform

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str1 = new String('Geeks'); 
    var str2 = new String('for'); 
    var str3 = new String('Geeks'); 

    // Combines the text of two strings and 
    // returns a new string.
    var str = str2.concat(str3.toString())
    str = str1.concat(str.toString())
    console.log("Concatenated String : " + str);
</script>
```

**输出:**

```
Concatenated String : GeeksforGeeks
```