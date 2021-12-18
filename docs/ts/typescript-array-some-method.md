# 排版|数组点阵法

> 原文:[https://www.geeksforgeeks.org/typescript-array-some-method/](https://www.geeksforgeeks.org/typescript-array-some-method/)

**Array.some()** 是一个内置的 TypeScript 函数，用于检查数组中的某个元素是否通过了提供的函数实现的测试。
**语法:**

```
array.some(callback[, thisObject])
```

**参数:**该方法接受如上所述和如下所述两个参数:

*   **回调:**该参数是对每个元素进行测试的函数。
*   **thisObject :** 此参数是执行回调时用作此的对象。

**返回值:**如果这个数组中的某个元素满足提供的测试函数，这个方法返回 true。
下面的例子说明了**数组中的**方法:
**例子 1:**

## 以打字打的文件

```
// check for positive number 
function ispositive(element, index, array)
{ 
   return element > 0;
} 

// Driver code
var arr = [ 11, 89, 23, 7, 98 ]; 

// check for positive number 
var value = arr.some(ispositive); 
console.log( value );
```