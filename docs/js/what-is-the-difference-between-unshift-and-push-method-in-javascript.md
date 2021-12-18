# JavaScript 中 unshift()和 Push()方法有什么区别？

> 原文:[https://www . geesforgeks . org/unshift 和 push-in-method-JavaScript 的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-unshift-and-push-method-in-javascript/)

JavaScript**[**Unshift()**](https://www.geeksforgeeks.org/javascript-array-unshift-method/)方法与 [**push()**](https://www.geeksforgeeks.org/javascript-array-push-method/) 方法非常相似，但区别在于 **unshift()** 方法在数组的最开始添加元素，而 **push()** 方法在数组的末尾添加元素。**

**以下几点列出了常见的问题。**

**这两种方法都用于将元素添加到数组中。**

*   **这两种方法都通过添加到数组中的元素数量来改变数组的长度。**
*   **这两种方法都用于增加数组的长度。**
*   ****unshift()** 和 **push()** 都是对象数组的内置方法。**
*   **这两种方法都会改变原始数组。**
*   **这两个方法都返回新添加的元素。**

**【Unshift()和 Push()的区别:**

**略有不同的是， **unshift()** 方法将 0 索引处的元素相加，通过最终返回数组的长度，所有的值都移动了 1。 **push()** 方法返回从最后一个索引添加新元素的最后一个元素。**

****例:**下面是数组 **unshift()** 方法的例子。**

## **java 描述语言**

```
<script> 
function func() { 

    // Original array 
    var array = ["GFG", "Geeks", "for", "Geeks"]; 

    // Checking for condition in array 
    var value = array.unshift("GeeksforGeeks"); 

    document.write(value); 
    document.write("<br />"); 
    document.write(array); 
} 

func(); 
</script> 
```

****输出:****

```
GeeksforGeeks,GFG,Geeks,for,Geeks. 
```

****例 2:** 下面是阵**推()**法的例子。**

## **java 描述语言**

```
<script> 
    function func() { 
        var arr = ['GFG', 'gfg', 'g4g']; 

        // Pushing the element into the array 
        arr.push('GeeksforGeeks'); 
                document.write(arr); 

    } 
    func(); 
</script>                 
```

****输出:****

```
***GFG,gfg,g4g,GeeksforGeeks*** 
```