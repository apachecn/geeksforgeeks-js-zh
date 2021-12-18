# JavaScript 中的 every()和 some()方法有什么区别？

> 原文:[https://www . geeksforgeeks . org/JavaScript 中的每种方法和某些方法的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-every-and-some-methods-in-javascript/)

JavaScript 中的 **[Array.every()](https://www.geeksforgeeks.org/javascript-array-prototype-every-function/)** 方法用于检查数组中的所有元素是否满足给定条件。

JavaScript 中的 **[Array.some()](https://www.geeksforgeeks.org/javascript-array-prototype-function/)** 方法用于检查数组中至少有一个元素是否满足给定条件。

唯一的区别是 **some()** 方法如果任何谓词为真将返回 true，而 **every()** 方法如果所有谓词为真将返回 true。

**示例 1:** 本示例实现了 some()方法。

```
<script>

// JavaScript code for some() function 
function isodd(element, index, array) {  
    return (element % 2 == 1);  
} 

function geeks() { 
    var arr = [ 6, 1, 8, 32, 35 ]; 

    // check for odd number 
    var value = arr.some(isodd); 
    console.log(value); 
} 
geeks(); 
</script>
```

**输出:**

```
true
```

**示例 2:** 本示例实现了 every()方法。

```
<script>

// JavaScript code for every() function 
function isodd(element, index, array) {  
    return (element % 2 == 1);  
} 

function geeks() { 
    var arr = [ 6, 1, 8, 32, 35 ]; 

    // check for odd number 
    var value = arr.every(isodd); 
    console.log(value); 
} 
geeks(); 
</script>
```

**输出:**

```
false
```