# 如何在 JavaScript 中不用数学函数找到最小值/最大值？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中查找不带数学函数的最小值和最大值/](https://www.geeksforgeeks.org/how-to-find-min-max-values-without-math-functions-in-javascript/)

在本文中，我们将学习如何在不使用数学函数的情况下找到数组中的最小值和最大值。我们知道 **Math.max()** 返回数组中传递的最大值，而 **Math.min()** 返回传递的最小值。

**方法:**数学函数的相同功能可以使用循环来实现，该循环将迭代数组中存在的数字，以找到数组中的最大值和最小值。

我们将继续使用循环检查数组中的所有元素。如果我们发现任何元素大于先前的“最大”值，我们将该值设置为最大值。同样，我们继续检查任何小于“最小值”的元素。如果我们得到任何这样的元素，我们用一个较小的值替换“min”的值。因此，使用循环函数，我们可以得到在数组/列表中输入的最大值和最小值。

下面的例子将演示上述方法。

**例:**

## JavaScript

```
<script>

    // Array of numbers where the maximum
    // and minimum are to be found
    const array = [-1, 2, -5, 8, 16];

    // Setting a number of the given array as
    // value of max and min we choose 0th index
    // element as atleast one element should be
    // present in the given array

    let max = array[0], min = array[0];
    for (let i = 0; i < array.length; i++) {

        // If we get any element in array greater
        // than max, max takes value of that
        // larger number
        if (array[i] > max) { max = array[i]; }

        // If we get any element in array smaller
        // than min, min takes value of that
        // smaller number
        if (array[i] < min) { min = array[i]; }
    }
    console.log("max = " + max);
    console.log("min = " + min);
</script>
```

**输出:**使用该方法找到数组的最大值和最小值。

```
max = 16
min = -5
```