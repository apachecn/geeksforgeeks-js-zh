# JavaScript 数组排序()方法

> 原文:[https://www.geeksforgeeks.org/javascript-array-sort-method/](https://www.geeksforgeeks.org/javascript-array-sort-method/)

下面是**数组排序()**方法的例子。

*   **节目 1:**

    ```
    <script>
    // JavaScript to illustrate sort() function
    function func() {

        // Original string
        var arr = ["Geeks", "for", "Geeks"]

        document.write(arr);
        document.write("<br>");
        // Sorting the array
        document.write(arr.sort());
    }
    func();
    </script>
    ```

*   **输出:**

    ```
    Geeks,for,Geeks
    Geeks,Geeks,for

    ```

**arr.sort()** 方法用于根据 **compare()** 功能按照给定的顺序对数组进行排序。如果省略该方法，则该数组按**升序**排序。
**语法:**

```
arr.sort(compareFunction)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **compareFunction:** 此参数用于根据不同的属性和不同的顺序对元素进行排序。
    *   compareFunction(a,b) < 0

        那么答案中 a 在 b 之前。

    *   compareFunction(a,b) > 0

        那么在答案中，b 在 a 之前。

    *   compareFunction(a,b) = 0

        那么 a 和 b 的顺序保持不变。

**返回值:**该方法返回排序后的原始数组的引用。

以下示例说明了 JavaScript 数组排序()方法:

*   **Example 1:** In this example the **sort()** method arranges the elements of the array in ascending order.

    ```
    var arr = [2, 5, 8, 1, 4]
    document.write(arr.sort());
    document.write(arr);

    ```

    **输出:**

    ```
    1,2,4,5,8
    1,2,4,5,8

    ```

    *   **Example 2:** In this example the **sort()** method the elements of the array are sorted according the function applied on each element.

    ```
    var arr = [2, 5, 8, 1, 4]
    document.write(arr.sort(function(a, b) {
      return a + 2 * b;
    }));
    document.write(arr);

    ```

    **输出:**

    ```
    2,5,8,1,4
    2,5,8,1,4

    ```

    上述方法的代码如下:
    **程序 1:**

    ```
    <script>
    // JavaScript to illustrate sort() function
    function func() {

        //Original string
        var arr = [2, 5, 8, 1, 4]

        //Sorting the array
        document.write(arr.sort());
        document.write("<br>");
        document.write(arr);
    }
    func();
    </script>
    ```

    **输出:**

    ```
    1,2,4,5,8
    1,2,4,5,8

    ```

    **程序 2:**

    ```
    <script>
    // JavaScript to illustrate sort() function

    function func() {

        // Original array
        var arr = [2, 5, 8, 1, 4];

        document.write(arr.sort(function(a, b) {
        return a + 2 * b;
    }));
    document.write("<br>");
    document.write(arr);
    }
    func();
    </script>
    ```

    **输出:**

    ```
    4,1,8,5,2
    4,1,8,5,2

    ```

    **支持的浏览器:**JavaScript Array sort()方法支持的浏览器如下:

    *   谷歌 Chrome 1 及以上版本
    *   边缘 12 及以上
    *   Firefox 1 及以上版本
    *   Internet Explorer 5.5 及以上版本
    *   歌剧 4 及以上
    *   Safari 1 及以上