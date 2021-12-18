# JavaScript 中 Shift() vs pop()方法

> 原文:[https://www . geesforgeks . org/shift-vs-pop-method-in-JavaScript/](https://www.geeksforgeeks.org/shift-vs-pop-method-in-javascript/)

JavaScript **shift()和 pop()** 方法用于从数组中移除元素。但是它们之间有一点区别。 **Shift()** 方法移除第一个元素，而 **pop()** 方法移除数组中的最后一个元素。

*   **Shift()** 返回数组中移除的第一个元素。如果数组是空的，那么这个函数返回未定义，而 **pop()** 方法将移除的元素数组。如果数组是空的，那么这个函数返回 undefined。
*   这两种方法都用于将数组的长度减少 1。
*   **shift()** 和 **pop()** 都是对象数组的内置方法。
*   这两种方法都会改变原始数组。

**例:**以下为阵**移()**法**例。**

## java 描述语言

```
<script> 
function func() { 

    // Original array 
    var array = ["GFG", "Geeks", "for", "Geeks"]; 

    // Checking for condition in array 
    var value = array.shift(); 

    document.write(value); 
    document.write("<br />"); 
    document.write(array); 
} 

func(); 
</script> 
```

**输出:**

```
GFG
Geeks, for, Geeks
```

**例 2:** 下面是 **pop()** 法的阵例。

## java 描述语言

```
<script> 
    function func() { 
        var arr = ['GFG', 'gfg', 'g4g', 'GeeksforGeeks']; 

        // Popping the last element from the array 
        document.write(arr.pop());
    } 
    func(); 
</script>                 
```

**输出:**

```
GeeksforGeeks
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软边缘
*   Mozilla Firefox
*   旅行队
*   歌剧