# JavaScript 数组点阵法

> 原文:[https://www.geeksforgeeks.org/javascript-array-some-method/](https://www.geeksforgeeks.org/javascript-array-some-method/)

下面是**数组 some()** 方法的例子。

*   **例:**

    ```
    <script>
        function checkAvailability(arr, val) {
            return arr.some(function (arrVal) {
                return val === arrVal;
            });
        }
        function func() {
            // Original function
            var arr = [2, 5, 8, 1, 4];

            // Checking for condition
            document.write(checkAvailability(arr, 2));
            document.write("<br>");
            document.write(checkAvailability(arr, 87));
        }
        func();
    </script>
    ```

*   **输出:**

    ```
    true
    false

    ```

**arr.some()** 方法检查数组的至少一个元素是否满足参数方法检查的条件。

**语法:**

```
arr.every(callback(element[, index[, array]])[, thisArg])
```

**参数:**该方法接受五个参数，如上所述，如下所述:

*   **回调:**该参数保存数组每个元素要调用的函数。
*   **元素:**参数保存当前正在处理的元素的值。
*   **索引:**这个参数是可选的，它保存数组中从 0 开始的 currentValue 元素的索引。
*   **数组:**这个参数是可选的，它保存了调用 array . after 的完整数组。
*   **thisArg:** 这个参数是可选的，它保存要传递的上下文，以便在执行回调函数时使用。如果传递了上下文，它将像这样用于回调函数的每次调用，否则使用 undefined 作为默认值。

**返回值:**此方法返回 **true** 即使数组的一个元素满足参数方法实现的条件(并且不检查剩余值)。如果数组中没有元素满足条件，则返回**假**。

下面的例子说明了 JavaScript 中的方法:

*   **Example 1:** In this example the method **some()** checks for any number that is greater than **5**. Since there exists element that satisfy this condition, thus the method returns **true**.

    ```
    function isGreaterThan5(element, index, array) 
    {
      return element > 5;
    }

    print([2, 5, 8, 1, 4].some(isGreaterThan5));

    ```

    **输出:**

    ```
    true

    ```

*   **Example 2:** In this example the method **some()** checks for any number that is greater than **5**. Since there exists no elements that satisfy this condition, thus the method returns **false**.

    ```
    function isGreaterThan5(element, index, array) 
    {
      return element > 5;
    }

    print([-2, 5, 3, 1, 4].some(isGreaterThan5)); 

    ```

    **输出:**

    ```
    false

    ```

*   **Example 3:** In this example the method **some()** checks for **2** and **87** in the array. Since only **2** is available therefore the method returns **true** for first query while it returns **false** for second query.

    ```
    var arr = [2, 5, 8, 1, 4]

    function checkAvailability(arr, val) 
    {
      return arr.some(
               function(arrVal) 
               {
                 return val === arrVal;
               } );
    }

    print(checkAvailability(arr, 2));
    print(checkAvailability(arr, 87));

    ```

    **输出:**

    ```
    true
    false

    ```

上述方法的代码如下:

**程序 1:**

```
<script>
    function isGreaterThan5(element, index, array) {
        return element > 5;
    }
    function func() {
        // Original array
        var array = [2, 5, 8, 1, 4];

        // Checking for condition in array
        var value = array.some(isGreaterThan5);

        document.write(value);
    }
    func();
</script>
```

**输出:**

```
true

```

**程序 2:**

```
<script>
    function isGreaterThan5(element, index, array) {
        return element > 5;
    }

    function func() {
        // Original array
        var array = [-2, 5, 3, 1, 4];

        // Checking for condition in the array
        var value = array.some(isGreaterThan5);

        document.write(value);
    }

    func();
</script>
```

**输出:**

```
false

```

**支持的浏览器:**JavaScript**Array some()**方法支持的浏览器如下:

*   谷歌 Chrome 1 以上
*   边缘 12 及以上
*   Firefox 1.5 及以上版本
*   Internet Explorer 9 及以上版本
*   Opera 9.5 及以上
*   Safari 3 及以上版本