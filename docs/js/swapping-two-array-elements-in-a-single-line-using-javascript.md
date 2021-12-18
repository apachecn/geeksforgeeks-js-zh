# 使用 JavaScript 在一行中交换两个数组元素

> 原文:[https://www . geeksforgeeks . org/swapping-单行双数组元素-使用-javascript/](https://www.geeksforgeeks.org/swapping-two-array-elements-in-a-single-line-using-javascript/)

在 JavaScript 中，有许多方法可以用来交换两个数组元素。在本文中，我们将讨论一种在一行中交换 JavaScript 中两个数组元素的方法。输入和输出如下。

```
Input: arr = { 10, 20, 40, 30 }
Output: arr = { 10, 20, 30, 40 } 
// Swapped 30 and 40
```

这种交换可以通过将我们想要反转的 2 个数组元素按顺序写在左边的方括号中来完成。在右侧，我们将写入相同的数组元素，但这次是以相反的顺序。

**语法:**

```
[a[m], a[n]] = [a[n], a[m]] 

// where m and n are the index numbers to swap
```

**例 1:**

## java 描述语言

```
<script>
  let arr = [1, 2, 3, 5, 4];

  // Swapping element at index 3 with index 4
  [arr[3], arr[4]] = [arr[4], arr[3]]

  // Print the array
  console.log(arr)
</script>
```

**输出:**

```
[1, 2, 3, 4, 5]
```

**例二:**

## Javascript

```
<script>
  let arr = ["e", "b", "c", "d", "a"];

  // Swapping element at index 0 with index 4
  [arr[0], arr[4]] = [arr[4], arr[0]];

  // Print the array
  console.log(arr);
</script>
```

**输出:**

```
['a','b','c','d','e']
```