# 如何在 JavaScript 中将给定数组展平到指定深度？

> 原文:[https://www . geesforgeks . org/如何将给定数组展平到指定深度 javascript/](https://www.geeksforgeeks.org/how-to-flatten-a-given-array-up-to-the-specified-depth-in-javascript/)

在本文中，我们将学习如何在 JavaScript 中将给定的数组展平到指定的深度。

JavaScript 中的 **[flat()方法](https://www.geeksforgeeks.org/javascript-array-flat-method/)** 用于将数组展平到所需的深度。它创建一个新的数组，并将原始数组的子数组递归连接到给定的深度。此方法接受的唯一参数是可选的深度参数(默认为 1)。此方法也可用于从数组中移除空元素。

**语法:**

```
array.flat(depth);
```

**示例:**

## 超文本标记语言

```
<html>
  <body>
    <h1 style="color: green;">
      GeeksforGeeks
    </h1>
    <b>
      How to flatten a given array up to 
      the specified depth in JavaScript?
    </b>
    <script>

      // Define the array
      let arr = [1, [2, [3, [4, 5], 6], 7, 8], 9, 10];

      console.log("Original Array:", arr);

      let flatArrOne = arr.flat();

      console.log(
        "Array flattened to depth of 1:",
        flatArrOne
      );

      let flatArrTwo = arr.flat(2);

      console.log(
        "Array flattened to depth of 2:",
        flatArrTwo
      );

      let flatArrThree = arr.flat(Infinity);

      console.log(
        "Array flattened completely:",
        flatArrThree
      );
    </script>
  </body>
</html>
```

**输出:**

```
Original Array: [1, [2, [3, [4, 5], 6], 7, 8], 9, 10]
Array flattened to depth of 1: [1, 2, [3, [4, 5], 6], 7, 8, 9, 10]
Array flattened to depth of 2: [1, 2, 3, [4, 5], 6, 7, 8, 9, 10]
Array flattened completely: [1, [2, [3, [4, 5], 6], 7, 8], 9, 10]
```