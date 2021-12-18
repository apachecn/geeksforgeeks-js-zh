# 类型脚本|数组索引 Of()方法

> 原文:[https://www . geesforgeks . org/typescript-array-indexof-method/](https://www.geeksforgeeks.org/typescript-array-indexof-method/)

**Array.indexOf()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于查找作为函数参数提供的搜索元素的第一次出现的索引。
**语法:**

```
array.indexOf(searchElement[, fromIndex])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **searchElement :** 此参数是要在数组中定位的元素。
*   **fromIndex :** 此参数是开始搜索的索引。

**返回值:**这个方法返回找到的元素的索引。
以下示例说明了 TypeScript 中的**数组 indexOf()** 方法。

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of indexOf() method 
    var val = arr.indexOf(7)

    // printing element
    console.log(val);
</script>
```

**输出:**

```
3

```

**例 2:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 'a','b','c','a','e' ]; 

    // use of indexOf() method 
    var val = arr.indexOf('a',4)

    // printing element
    console.log(val);
</script>
```

**输出:**

```
-1

```