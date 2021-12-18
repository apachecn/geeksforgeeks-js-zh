# JavaScript 数组 pop()方法

> 原文:[https://www.geeksforgeeks.org/javascript-array-pop-method/](https://www.geeksforgeeks.org/javascript-array-pop-method/)

下面是**数组 pop()** 方法的例子。

*   **例:**

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

*   **输出:**

    ```
    GeeksforGeeks
    ```

**arr.pop()** 方法用于移除数组的最后一个元素，并返回移除的元素。该功能通过 **1** 减少数组长度。

**语法:**

```
arr.pop()
```

**参数:**此方法不接受任何参数。

**返回值**该方法返回删除的元素数组。如果数组为空，则该函数返回**未定义**。

以下示例说明了 JavaScript 数组 pop()方法:

*   **Example 1:** In this example the **pop()** method removes the last element from the array, which is **4** and returns it.

    ```
    var arr = [34, 234, 567, 4];
    var popped = arr.pop();
    print(popped);
    print(arr);

    ```

    **输出:**

    ```
    4
    34,234,567

    ```

*   **Example 2:** In this example the function **pop()** tries to extract the last element of the array but since the array is empty therefore it returns **undefined** as the answer.

    ```
    var arr = [];
    var popped = arr.pop();
    print(popped);

    ```

    **输出:**

    ```
    undefined
    ```

上述方法的更多示例代码如下:

**程序 1:**

```
<script>
function func() {
    var arr = [34, 234, 567, 4];

    // Popping the last element from the array 
    var popped = arr.pop();
    document.write(popped);
    document.write("<br>");
    document.write(arr);
}
func();
</script>
```

**输出:**

```
4
34,234,567

```

**程序 2:**

```
<script>
function func() {

    var arr = [];

    // popping the last element
    var popped = arr.pop();
    document.write(popped);
}
func();
</script>
```

**输出:**

```
undefined
```

**支持的浏览器:**JavaScript**数组 pop()** 方法支持的浏览器如下:

*   谷歌 Chrome 1.0 及以上版本
*   微软 Edge 12 及以上版本
*   Mozilla Firefox 1.0 及以上版本
*   Safari 1 及以上
*   歌剧 4 及以上