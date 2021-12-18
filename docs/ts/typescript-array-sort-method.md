# 类型脚本|数组排序()方法

> 原文:[https://www.geeksforgeeks.org/typescript-array-sort-method/](https://www.geeksforgeeks.org/typescript-array-sort-method/)

**Array.sort()** 是一个内置的 TypeScript 函数，用于对数组的元素进行排序。
**语法:**

```
array.sort( compareFunction )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **比较函数:**该参数是定义排序顺序的函数

**返回值:**该方法返回排序后的数组。

以下示例说明了 TypeScriptJS 中的**数组排序()**方法:
**示例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of sort() method 
    var val = arr.sort();

    // printing
    console.log( val );
</script>
```

**输出:**

```
[ 11, 23, 7, 89, 98 ]

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = ["G", "e", "e", "k", "s", "f", "o", "r", 
               "g", "e", "e", "k", "s"]; 
    var val;

    // use of sort() method 
    val = arr.sort();
    console.log( val );
</script>
```

**输出:**

```
[ 'G', 'e', 'e', 'e', 'e', 'f', 'g', 'k', 'k', 'o', 'r', 's', 's' ]

```