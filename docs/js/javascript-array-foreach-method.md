# JavaScript 数组 forEach()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-foreach-method/](https://www.geeksforgeeks.org/javascript-array-foreach-method/)

下面是**数组 forEach()** 方法的例子。

*   **例:**

    ```
    <script>
        // JavaScript to illustrate forEach() method
        function func() {

            // Original array
            const items = [12, 24, 36];
            const copy = [];

            items.forEach(function (item) {
                copy.push(item + item+2);
            });

            document.write(copy);
        }
        func();
    </script>                    
    ```

*   **输出:**

    ```
    26,50,74
    ```

**arr.forEach()** 方法为数组的每个元素调用一次提供的函数。所提供的函数可以对给定数组的元素执行任何类型的操作。

**语法:**

```
array.forEach(callback(element, index, arr), thisValue)
```

**参数:**该方法接受五个参数，如上所述，如下所述:

*   **回调:**该参数保存数组每个元素要调用的函数。
*   **元素:**参数保存当前正在处理的元素的值。
*   **索引:**这个参数是可选的，它保存数组中当前值元素从 0 开始的索引。
*   **数组:**这个参数是可选的，它保存了调用 array . after 的完整数组。
*   **thisArg:** 这个参数是可选的，它保存要传递的上下文，以便在执行回调函数时使用。如果传递了上下文，它将像这样用于回调函数的每次调用，否则使用 undefined 作为默认值。

**返回值:**这个方法的返回值总是**未定义**。此方法可能会也可能不会更改提供的原始数组，因为它取决于参数函数的功能。

下面的例子说明了 JavaScript 中的数组 forEach()方法:

*   **Example:** In this example the method **forEach()** calculates the square of every element of the array.

    ```
    const items = [1, 29, 47];
    const copy = [];

    items.forEach(function(item){
      copy.push(item*item);
    });
    print(copy);

    ```

    **输出:**

    ```
    1,841,2209
    ```

下面提供了上述方法的代码:

**程序:**

```
<script>
    // JavaScript to illustrate forEach() method
    function func() {

        // Original array
        const items = [1, 29, 47];
        const copy = [];

        items.forEach(function (item) {
            copy.push(item * item);
        });

        document.write(copy);
    }
    func();
</script>
```

**输出:**

```
1,841,2209
```

**支持的浏览器:**JavaScript**Array forEach()**方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1.5 及以上版本
*   Internet Explorer 9 及以上版本
*   Opera 9.5 及以上
*   Safari 3 及以上版本