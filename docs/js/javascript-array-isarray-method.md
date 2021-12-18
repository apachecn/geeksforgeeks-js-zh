# JavaScript 数组 isArray()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-isarray-method/](https://www.geeksforgeeks.org/javascript-array-isarray-method/)

下面是**数组 isArray()** 方法的例子。

*   **例:**

    ```
    <script>
        // JavaScript code for isArray() function
        function func() {
            document.write(Array.isArray('foobar'));
        }

       func();
    </script>
    ```

*   **输出:**

    ```
    false
    ```

**arr.isArray()** 方法确定传递给该函数的值是否为数组。如果传递的参数是数组，则该函数返回 true，否则返回 false。

**语法:**

```
Array.isArray(obj)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **obj:** 此参数保存将要测试的对象。

**返回值:**如果传递的参数是数组，则该函数返回布尔值 true，否则返回 false。

下面的例子说明了 JavaScript 中的**数组 isArray()** 方法:

*   **示例 1:** 由于传递给函数**的参数 isArray()** 是一个数组，因此该函数返回 **true** 作为答案。

    ```
    Input : print(Array.isArray(['Day','Night','Evening']));
    Output: true

    ```

*   **示例 2:** 由于传递给函数**的参数 isArray()** 是一个地图，因此该函数返回 **false** 作为答案。

    ```
    Input : print(Array.isArray({foo: 123}));
    Output: false

    ```

*   **示例 3:** 由于传递给函数**的参数 isArray()** 是一个字符串，因此该函数返回 **false** 作为答案。

    ```
    Input : print(Array.isArray('foobar'));
    Output: false

    ```

下面提供了上述方法的代码:

**程序 1:**

```
<script>
    // JavaScript code for isArray() function
    function func() {
        document.write(Array.isArray(['Day','Night','Evening']));
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
    // JavaScript code for isArray() function
    function func() {
        document.write(Array.isArray({foo: 123}));
    }
    func();
</script>
```

**输出:**

```
false
```

**支持的浏览器:**JavaScript**Array isArray()**方法支持的浏览器如下:

*   谷歌 Chrome 5.0
*   微软边缘 12
*   Mozilla Firefox 4.0
*   Safari 5.0
*   歌剧 10.5