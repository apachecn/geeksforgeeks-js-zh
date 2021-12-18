# 如何在 JavaScript 中从数组中获取 n 个最大的元素？

> 原文:[https://www . geesforgeks . org/如何从 javascript 数组中获取 n 个最大元素/](https://www.geeksforgeeks.org/how-to-get-n-largest-elements-from-array-in-javascript/)

在本文中，我们将看到如何使用 Javascript 从数组中找到 n 个最大元素

**示例:**

```
Input: arr = [1, 2, 3, 4, 5, 6], n = 3;
Output: 4, 5, 6
Explanation: Here we will see the 3 largest 
    elements in the given array are 4, 5, 6.

Input: arr = [5, 76, 32, 98, 52, 57] n = 2;
Output: 98 , 76
```

**蛮力方法:**我们首先制作一个名为 largArr 的数组，长度等于 n。然后对于 largArr 的每个索引，我们将逐个填充 Arr 中的元素

例如:如果我们有 n=3，那么数组 **largArr** 的长度将等于 3，然后我们将运行 **for 循环**一个接一个地填充 largArr 中的元素。

**实施:**

## java 描述语言

```
<script>
    var largArr = new Array();
    var arr = new Array(93, 17, 56, 91,
        98, 33, 9, 38, 55, 78, 29, 81, 60);

    function largest() {
        largArr[0] = 0;
        largArr[1] = 0;
        largArr[2] = 0;

        for (i = 0; i < arr.length; i++) {
            if (arr[i] > largArr[0]) {
                largArr[0] = arr[i];

            }
        }

        for (i = 0; i < arr.length; i++) {
            if (arr[i] > largArr[1]
                && arr[i] < largArr[0]) {
                largArr[1] = arr[i];

            }
        }

        for (i = 0; i < arr.length; i++) {
            if (arr[i] > largArr[2]
                && arr[i] < largArr[1]) {
                largArr[2] = arr[i];
            }
        }

        console.log(largArr[0]);
        console.log(largArr[1]);
        console.log(largArr[2]);
    }

    largest();
</script>
```

**输出:**

```
98 93 91
```

**优化解决方案:**我们首先按降序对数组进行排序，然后运行长度等于 n 的循环，并打印前 n 个最大的元素。

**实施:**

## java 描述语言

```
<script>
    var largArr = new Array();
    var arr = new Array(93, 17, 56, 91, 98,
            33, 9, 38, 55, 78, 29, 81, 60);

    findLargest3();

    function findLargest3() {
        arr.sort((a, b) => a < b ?
            1 : a > b ? -1 : 0);

        console.log(arr[0]);
        console.log(arr[1]);
        console.log(arr[2]);

        console.log(arr.slice(0, 3));
    }
</script>
```

**输出:**

```
 98
 93
 91
 [98,93,91]
```