# 类型脚本|数组 toString()方法

> 原文:[https://www . geesforgeks . org/typescript-array-tostring-method/](https://www.geeksforgeeks.org/typescript-array-tostring-method/)

**Array.toString()** 是一个内置的 TypeScript 函数，用于获取表示指定数组及其元素的源代码的字符串。
**语法:**

```
array.toString()
```

**参数:**此方法不接受任何参数。

**返回值:**这个方法返回代表数组的字符串。

下面的示例说明了 TypeScriptJS 中的**字符串 toString()** 方法:

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of toString() method 
    var tring= arr.toString();

    // printing
    console.log(tring);
</script>
```

**输出:**

```
11,89,23,7,98

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = ["G", "e", "e", "k", "s", "f", "o", 
               "r", "g", "e", "e", "k", "s"]; 
    var val;

    // use of toString() method 
    val = arr.toString();
    console.log( val );
</script>
```

**输出:**

```
G,e,e,k,s,f,o,r,g,e,e,k,s

```