# TypeScript | String to localelowercase()方法

> 原文:[https://www . geesforgeks . org/typescript-string-tolocalelowercase-method/](https://www.geeksforgeeks.org/typescript-string-tolocalelowercase-method/)

**toLocaleLowerCase()** 是 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的内置函数，用于将字符串中的字符转换为小写，同时考虑当前的区域设置。

**语法:**

```
string.toLocaleLowerCase( ) 
```

**参数:**该方法不接受任何参数。
**返回值:**该方法返回当前区域设置的小写字符串。
以下示例说明了 TypeScript 中的 String toLocaleLowerCase()方法
**示例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String toLocaleLowerCase() Method
    var newstr = str.toLocaleLowerCase() 
    console.log(newstr);
</script>
```