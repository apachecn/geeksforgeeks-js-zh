# JavaScript 数组 copy inner()方法

> 原文:[https://www . geesforgeks . org/JavaScript-array-copy inner-method/](https://www.geeksforgeeks.org/javascript-array-copywithin-method/)

下面是**数组 copy inner()**方法的例子。

*   **Example:**

## Javascript

```
<script>
    // Input array
    var array = [1, 2, 3, 4, 5, 6, 7];

    // placing at index position 0 the element
    // between index 3 and 6
    document.write("Array " + array.copyWithin(0, 3, 6));
</script>
```

**输出:**

```
Array 4, 5, 6, 4, 5, 6, 7
```

**arr . copyin()**方法将数组的一部分复制到同一个数组中并返回，而不修改其大小，即复制同一个数组中的数组元素。

**语法:**

```
array.copyWithin(target, start, end)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Target:** The index position where the element is to be copied (required).
*   **Start:** Optional. The index position of the element to start copying (default value is 0).
*   **End:** Optional. The index position of the stop copying element (the default value is array.length).

**返回值:**返回修改后的数组。

上述方法的更多示例代码如下:

**程序一:**

## Javascript

```
<script>
    // Input array
    var array = [1, 2, 3, 4, 5, 6, 7];

    // Placing from index position 0 the
    // Element from index 4
    document.write("Array " + array.copyWithin(0, 4));
</script>
```

**输出:**

```
Array 5, 6, 7, 4, 5, 6, 7
```

**程序二:**

## Javascript

```
<script>
    // Input array
    var array = [1, 2, 3, 4, 5, 6, 7];

    // Placing from index position 3
    // The element from index 0
    document.write("Array " + array.copyWithin(3));
</script>
```

**输出:**

```
Array 1, 2, 3, 1, 2, 3, 4
```

**应用程序:**每当我们需要将任何数组的内容复制到同一个数组时，我们都会在 JavaScript 中使用 arr . copy inner()元素。

## Javascript

```
<script>
    // Input array
    var array = [1, 2, 3, 4, 5, 6, 7];

    // Placing at index position 0 the
    // Element between index 4 and 5
    document.write("Array " + array.copyWithin(0, 4, 5));
</script>
```

**输出:**

```
Array 5, 2, 3, 4, 5, 6, 7
```

**支持的浏览器:**JavaScript**Array copy inner()**方法支持的浏览器如下:

*   Microsoft Edge 12.0
*   Mozilla Firefox 32.0
*   Opera 32.0
*   Safari 9