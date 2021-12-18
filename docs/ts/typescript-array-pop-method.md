# 类型脚本|数组 pop()方法

> 原文:[https://www.geeksforgeeks.org/typescript-array-pop-method/](https://www.geeksforgeeks.org/typescript-array-pop-method/)

**Array.pop()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于从数组中移除最后一个元素并返回该元素。
**语法:**

```
array.pop(); 
```

**参数:**该方法不接受任何参数。
**返回值:**这个方法返回从数组中移除的元素。
以下示例说明了 TypeScript 中的**数组 pop()** 方法。

**例 1:**

## Java Script 语言

```
<script>
    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ]; 

    // use of pop() method 
    var val = arr.pop()

    // printing element
    console.log( val );
</script>
```