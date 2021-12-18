# 类型脚本|数组隔()方法

> 原文:[https://www . geesforgeks . org/typescript-array-ever-method/](https://www.geeksforgeeks.org/typescript-array-every-method/)

**Array.every()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于检查数组中的所有元素是否通过了由提供的函数实现的测试。
**语法:**

```
array.every(callback[, thisObject])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **回调:**该参数是对每个元素进行测试的函数。
*   **thisObject :** 此参数是执行回调时用作此的对象。

**返回值:**如果这个数组中的每个元素都满足提供的测试函数，那么这个方法返回 true。
以下示例说明了打字稿中的**数组 every()** 方法

**例 1:**

## Java Script 语言

```
<script>
    // Check for positive number 
    function ispositive(element, index, array)
    { 
       return element > 0;
    } 

    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // Check for positive number 
    var value = arr.every(ispositive); 
    console.log( value );
</script>
```

**输出:**

```
true
```

**例 2:**

## Java Script 语言

```
<script>
    // Check for odd number 
    function isodd(element, index, array) 
    {  
       return (element % 2 == 1);  
    }   
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // Check for positive number 
    var value = arr.every(isodd); 
    console.log( value );
</script>
```

**输出:**

```
false
```