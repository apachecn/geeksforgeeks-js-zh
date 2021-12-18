# 如何在 JavaScript 中求给定数组所有元素的和？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中找到给定数组的所有元素之和/](https://www.geeksforgeeks.org/how-to-find-the-sum-of-all-elements-of-a-given-array-in-javascript/)

在本文中，我们将学习如何找到给定数组的所有元素/数字的总和。有许多方法可以解决下面通过例子描述的问题。

**示例 1:** 在本例中，我们将简单地使用 for 循环迭代数组的所有元素，以找到总和。

**档案名称:gfg . js**

## 【JavaScript】

```
<script>
    // Creating array
    var arr = [4, 8, 7, 13, 12]

    // Creating variable to store the sum
    var sum = 0;

    // Running the for loop
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }

    document.write("Sum is " + sum) // Prints: 44
</script>
```