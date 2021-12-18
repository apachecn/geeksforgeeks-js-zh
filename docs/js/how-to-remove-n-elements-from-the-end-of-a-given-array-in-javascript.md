# 如何在 JavaScript 中删除给定数组末尾的 n 个元素？

> 原文:[https://www . geesforgeks . org/如何从给定的 javascript 数组末尾移除 n 个元素/](https://www.geeksforgeeks.org/how-to-remove-n-elements-from-the-end-of-a-given-array-in-javascript/)

在本文中，我们将学习如何在 JavaScript 中从给定数组的末尾移除最后的 *n* 个元素。这可以通过两种方法实现:

JavaScript 中的 **[【拼接】()方法](https://www.geeksforgeeks.org/javascript-array-splice-method/)** 用于通过添加或移除数组中的元素来修改数组。此方法接受必须进行修改的索引和要删除的元素数量。可以通过从数组长度中减去元素的数量来找到必须开始删除的索引。

**语法:**

```
array.splice(start, deleteCount);
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
      How to remove n elements from the end
      of a given array in JavaScript?
    </b>
    <script>

      // Define the array
      let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

      console.log("Original Array:", arr);

      // Define the number of elements to remove
      let elemsToDelete = 3;

      // Using the splice() method to remove from
      // the last nth index for n elements
      arr.splice(arr.length - elemsToDelete,
                 elemsToDelete);

      console.log("Modified Array:", arr);
    </script>
  </body>
</html>
```

**输出:**

```
Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
Modified Array: [1, 2, 3, 4, 5, 6]
```

JavaScript 中的 **[pop()方法](https://www.geeksforgeeks.org/javascript-array-pop-method/)** 用于从数组中移除最后一个元素。这可以在 *n* 迭代的循环中重复，以在循环中使用*移除阵列的最后 *n* 个元素。*

**语法:**

```
array.pop();
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
      How to remove n elements from the end
      of a given array in JavaScript?
    </b>
    <script>

      // Define the array
      let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

      console.log("Original Array:", arr);

      // Define the number of elements to remove
      let elemsToDelete = 5;

      // Loop for the number of elements
      // to delete
      while (elemsToDelete--)

        // Pop the last element from the
        // end of the array
        arr.pop();

      console.log("Modified Array:", arr);
    </script>
  </body>
</html>
```

**输出:**

```
Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
Modified Array: [1, 2, 3, 4]
```