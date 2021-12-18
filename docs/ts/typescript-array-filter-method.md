# 类型脚本|数组过滤器()方法

> 原文:[https://www . geesforgeks . org/typescript-array-filter-method/](https://www.geeksforgeeks.org/typescript-array-filter-method/)

**Array.filter()** 是一个内置的 TypeScript 函数，用于创建一个新的数组，其中所有元素都通过了由提供的函数实现的测试。
**语法:**

```
array.filter(callback[, thisObject])
```

**参数:**该方法接受两个参数，如下所述:

*   **回调:**该参数是对每个元素进行测试的函数。
*   **thisObject :** 此参数是执行回调时用作此的对象。

**返回值:**该方法返回创建的数组。
以下示例说明了 TypeScript 中的**数组过滤器()**方法
**示例 1:**

## Java Script 语言

```
<script>
    // check for positive number 
    function ispositive(element, index, array)
    { 
       return element > 0;
    } 

    // Driver code
    var arr = [ 11, 89, -23, 7, 98 ]; 

    // check for positive number 
    var value = arr.filter(ispositive); 
    console.log( value );
</script>
```