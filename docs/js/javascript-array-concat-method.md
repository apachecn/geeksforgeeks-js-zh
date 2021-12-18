# JavaScript 数组 concat()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-concat-method/](https://www.geeksforgeeks.org/javascript-array-concat-method/)

下面是 **Array concat()** 方法连接三个数组的例子。

*   **例:**

    ```
    <script>
    // JavaScript code for concat() method
    function func() {
        var num1 = [11, 12, 13],
            num2 = [14, 15, 16],
            num3 = [17, 18, 19];
        document.write(num1.concat(num2, num3));
    }
    func();
    </script>
    ```

*   **输出:**

    ```
    [11,12,13,14,15,16,17,18,19]

    ```

**arr.concat()** 方法用于将两个或多个数组合并在一起。此方法不会改变作为参数传递的原始数组。

**语法:**

```
var new_array = old_array.concat(value1[, value2[, ...[, valueN]]])
```

**参数:**此方法的参数是需要添加到给定数组中的数组或值。此方法的参数数量取决于要合并的数组或值的数量。

**返回值:**该方法返回一个新创建的数组，该数组是在合并作为参数传递给该方法的所有数组后创建的。

以下示例说明了 JavaScript 数组 concat()方法:

*   **Example 1:** In this example, the method **concat()** concatenates all the three arrays into one array which it return as the answer.

    ```
    var num1 = [11, 12, 13],
        num2 = [14, 15, 16],
        num3 = [17, 18, 19];
    print(num1.concat(num2, num3));

    ```

    **输出:**

    ```
    [11,12,13,14,15,16,17,18,19]

    ```

*   **Example 2:** In this example, the method **concat()** concatenates all the arguments passed to the method with the given array into one array which it return as the answer.

    ```
    var alpha = ['a', 'b', 'c'];
    print(alpha.concat(1, [2, 3]));

    ```

    **输出:**

    ```
    [a,b,c,1,2,3]

    ```

*   **Example 3:** In this example, the method **concat()** concatenates both the arrays into one array which it return as the answer.

    ```
    var num1 = [[23]];
    var num2 = [89, [67]];
    print(num1.concat(num2));

    ```

    **输出:**

    ```
    [23,89,67] 

    ```

以上方法的更多示例代码如下:
**程序 1:**

```
<script>
    // JavaScript code for concat() method
    function func() {
        var alpha = ["a", "b", "c"];
        document.write(alpha.concat(1, [2, 3]));
    }
    func();
</script>
```

**输出:**

```
[a,b,c,1,2,3]
```

**程序 2:**

```
<script>
    // JavaScript code for concat() method
    function func() {
        var num1 = [[23]];
        var num2 = [89, [67]];
        document.write(num1.concat(num2));
    }
    func();
</script>
```

**输出:**

```
[23,89,67] 
```

**支持的浏览器:**JavaScript**Array concat()**方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上