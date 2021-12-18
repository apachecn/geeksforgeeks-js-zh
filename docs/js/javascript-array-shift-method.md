# JavaScript 数组移位()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-shift-method/](https://www.geeksforgeeks.org/javascript-array-shift-method/)

下面是**数组移位()**方法的例子。

*   **例:**

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

*   **输出:**

    ```
    GFG
    Geeks, for, Geeks
    ```

**arr.shift()** 方法移除数组的第一个元素，从而通过 **1** 减小原始数组的大小。

**语法:**

```
arr.shift()
```

**参数:**此方法不接受任何参数。

**返回值:**这个函数返回数组中被移除的第一个元素。如果数组为空，则该函数返回**未定义**。

**注意:**这个函数也可以和其他行为类似数组的 javascript 对象一起使用。

以下示例说明了 JavaScript 数组 shift()方法:

*   **Example 1:** In this example the **shift()** method removes the first element of the array, therefore it returns **34**.

    ```
    var arr = [2, 5, 8, 1, 4];
    document.write(value);
    document.write(arr);

    ```

    输出:

    ```
    34
    234,567,4

    ```

*   **Example 2:** In this example the **shift()** method tries to remove the first element of the array, but the array is empty, therefore it returns **undefined**.

    ```
    var arr = [];
    document.write(value);
    document.write(arr)

    ```

    **输出:**

    ```
    undefined
    ```

下面提供了上述方法的代码:

**程序 1:**

```
<script> 
function func() { 

    // Original array 
    var array = [34,234,567,4]; 

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
34
234,567,4

```

**程序 2:**

```
<script>
function func() { 

    // Original array 
    var array = []; 

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
undefined
```

**支持的浏览器:**JavaScript**数组 shift()** 方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上