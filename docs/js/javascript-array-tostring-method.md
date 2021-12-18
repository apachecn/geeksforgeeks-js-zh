# JavaScript 数组 toString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-tostring-method/](https://www.geeksforgeeks.org/javascript-array-tostring-method/)

下面是**数组 toString()** 方法的例子。

*   **例:**

    ```
    <script>
    // JavaScript to illustrate toString() method
    function func() {

        // Original array
        var arr = ["Geeks", "for", "Geeks"];

        // Creating a string
        var str = arr.toString();
        document.write(str);
    }
    func();
    </script>                    
    ```

*   **输出:**

    ```
    Geeks,for,Geeks
    ```

方法返回数组元素的字符串表示形式。
**语法:**

```
arr.toString()
```

**参数:**此方法不接受任何参数。

**返回值**该方法返回数组元素的字符串表示形式。如果数组为空，则返回一个空字符串。

下面的例子说明了 JavaScript 数组 toString()方法:

*   **Example 1:** In this example the **toString()** method creates a string consisting of array elements.

    ```
    var arr = [2, 5, 8, 1, 4]
    print(arr.toString());

    ```

    **输出:**

    ```
    2,5,8,1,4
    ```

下面提供了上述方法的代码:

**程序 1:**

```
<script>
// JavaScript to illustrate toString() method
function func() {

    // Original array
    var arr = [2, 5, 8, 1, 4];

    // Creating a string
    var str = arr.toString();
    document.write(str);
}
func();
</script>
```

**输出:**

```
2,5,8,1,4
```

**支持的浏览器:**JavaScript**Array toString()**方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上