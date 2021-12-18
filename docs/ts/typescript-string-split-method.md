# 类型脚本|字符串拆分()方法

> 原文:[https://www . geesforgeks . org/typescript-string-split-method/](https://www.geeksforgeeks.org/typescript-string-split-method/)

**split()** 是 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 中的一个内置函数，用于通过将字符串分成子字符串来将字符串对象拆分成字符串数组。

**语法:**

```
string.split([separator][, limit])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **分隔符**–该参数是用于分隔字符串的字符。
*   **限制**–该参数是整数，指定要查找的拆分数量的限制。

**返回值:**此方法返回新数组。
以下示例说明了 TypeScript 中的 String split()方法。
**例 1:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String split() Method
    var newarr = str.split(" "); 

    console.log(newarr);
</script>
```

**输出:**

```
[ 'Geeksforgeeks', '-', 'Best', 'Platform' ]

```

**例 2:**

## Java Script 语言

```
<script>
    // Original strings
    var str = "Geeksforgeeks - Best Platform"; 

    // use of String split() Method
    var newarr = str.split("",14); 

    console.log(newarr);
</script>
```

**输出:**

```
[ 'G', 'e', 'e', 'k', 's', 'f', 'o', 'r', 'g', 'e', 'e', 'k', 's', ' ' ]

```