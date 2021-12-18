# JavaScript 数组推送()方法

> 原文:[https://www.geeksforgeeks.org/javascript-array-push-method/](https://www.geeksforgeeks.org/javascript-array-push-method/)

下面是**阵推()**法的例子。

*   **例:**

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

*   **输出:**

    ```
    GFG,gfg,g4g,GeeksforGeeks
    ```

**arr.push()** 方法用于将一个或多个值推入数组。此方法通过添加到数组中的元素数量来更改数组的长度。

**语法:**

```
arr.push(element1, elements2 ....., elementN]])
```

**参数**此方法包含的参数数量与要插入数组的元素数量相同。

**返回值:**该方法在数组中插入参数后返回新的数组长度。

以下示例说明了 JavaScript 数组推送()方法:

*   **Example 1:** In this example the function **push()** adds the numbers to the end of the array.

    ```
    var arr = [34, 234, 567, 4];
    print(arr.push(23,45,56));
    print(arr);

    ```

    **输出:**

    ```
    7
    34,234,567,4,23,45,56

    ```

*   **Example 2:** In this example the function **push()** adds the objects to the end of the array.

    ```

    var arr = [34, 234, 567, 4];
    print(arr.push('jacob',true,23.45));
    print(arr);

    ```

    **输出:**

    ```
    7
    34,234,567,4,jacob,true,23.45

    ```

上述方法的更多示例代码如下:

**程序 1:**

```
<script>
function func() {

    // Original array
    var arr = [34, 234, 567, 4];

    // Pushing the elements
    document.write(arr.push(23,45,56));
    document.write("<br>");
    document.write(arr);
}
func();
</script>
```

**输出:**

```
7
34,234,567,4,23,45,56

```

**程序 2:**

```
<script>
function func() {

    var arr = [34, 234, 567, 4];

    document.write(arr.push('jacob',true,23.45));
    document.write("<br>");
    document.write(arr);
}
func();
</script>
```

**输出:**

```
7
34,234,567,4,jacob,true,23.45

```

**支持的浏览器:**JavaScript**数组推送()**方法支持的浏览器如下:

*   谷歌 Chrome 1.0 及以上版本
*   微软 Edge 12 及以上版本
*   Mozilla Firefox 1.0 及以上版本
*   Safari 1 及以上
*   歌剧 4 及以上