# JavaScript 数组扁平化()方法

> 原文:[https://www.geeksforgeeks.org/javascript-array-flat-method/](https://www.geeksforgeeks.org/javascript-array-flat-method/)

下面是**数组 flat()** 方法的例子。

*   **例:**

    ```
    <script>
        // Creating multilevel array
        const numbers = [['1', '2'], ['3', '4',
                         ['5',['6'], '7']]];

        const flatNumbers= numbers.flat(Infinity);
        document.write(flatNumbers);
    </script>
    ```

*   **ourtput:**t0]

**arr.flat()** 方法在 ES2019 中引入。它用于**展平**一个数组，以减少一个数组的嵌套。

**flat()** 方法在 JavaScript 的函数式编程范式中大量使用。在 JavaScript 中引入 **flat()** 方法之前，主要使用了**下划线. js** 等各种库。

**语法:**

```
arr.flat([depth])
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **深度:**它指定嵌套数组应该展平多深。如果没有传递深度值，默认值为 1，因为您认为它是一个可选参数。

**返回值:**返回一个数组，即**深度**比原数组平坦，它根据**深度**去除嵌套。

上述功能的更多代码定义如下:

**程序 1:** 下面的代码片段展示了 **flat()** 方法是如何工作的。

```
<script>
    let nestedArray = [1, [2, 3], [[]], 
                      [4, [5]], 6];

    let zeroFlat = nestedArray.flat(0);

    document.write(
      `Zero levels flattened array: ${zeroFlat}`);
    document.write("<br>");

    // 1 is the default value even
    // if no parameters are passed
    let oneFlat = nestedArray.flat(1);

    document.write(
      `One level flattened array: ${oneFlat}`);
    document.write("<br>");

    let twoFlat = nestedArray.flat(2);

    document.write(
      `One level flattened array: ${twoFlat}`);
    document.write("<br>");

    // No effect when depth is 3 or
    // more since array is already
    // flattened completely.
    let threeFlat = nestedArray.flat(3);
    document.write(
      `Three levels flattened array: ${threeFlat}`);
</script>
```

**输出:**

```
Zero levels flattened array: [1, [2, 3], [[]], [4, [5]], 6]
One level flattened array: [1, 2, 3, [], 4, [5], 6]
Two levels flattened array: [1, 2, 3, 4, 5, 6]
Three levels flattened array: [1, 2, 3, 4, 5, 6]

```

**注意:**对于深度大于 2 的，数组保持不变，因为它已经完全展平了。

**程序 2:** 我们也可以使用 **flat()** 方法移除数组中的空槽或空值。

```
<script>
    let arr = [1, 2, 3, , 4];
    let newArr = arr.flat();
    document.write(newArr);
</script>
```

**输出:**

```
[1, 2, 3, 4]
```

**支持的浏览器:**

*   谷歌 Chrome 69 及以上
*   边缘 79 及以上
*   Firefox 62 及以上版本
*   歌剧 56 及以上
*   Safari 12 及以上