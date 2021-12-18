# 类型脚本|数组 reduceRight()方法

> 原文:[https://www . geesforgeks . org/typescript-array-reduce right-method/](https://www.geeksforgeeks.org/typescript-array-reduceright-method/)

**Array.reduceRight()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于对数组的两个值应用一个函数，从而以从右到左的方式将其缩减为一个值。
**语法:**

```
array.reduceRight(callback[, initialValue])

```

**参数:**该方法接受如上所述和如下所述两个参数:

*   **回调:**此参数是对数组中的每个值执行的函数。
*   **initialValue :** 此参数是用作回调第一次调用的第一个参数的对象。

**返回值:**此方法返回数组的右缩减单值。
以下示例说明了 TypeScript 中的**数组 reduceRight()** 方法

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of reduceRight() method 
    var val = arr.reduceRight(function(a, b)
    { 
        return a - b; 
    });

    // printing element
    console.log( val );
</script>
```

**输出:**

```
-32

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [2, 5, 6, 3, 8, 9]; 
    var val;

    // use of reduceRight() method 
    val = arr.reduceRight(function(a, b)
    { 
        return a/b; 
    });

    // printing element
    console.log( val );
</script>
```

**输出:**

```
0.00625

```