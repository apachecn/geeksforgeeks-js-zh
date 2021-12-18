# 如何用 JavaScript 找到给定数组中除第一个元素以外的所有元素？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 在给定数组中查找除第一个元素之外的所有元素/](https://www.geeksforgeeks.org/how-to-find-all-elements-in-a-given-array-except-for-the-first-one-using-javascript/)

在本文中，我们将学习如何找到给定数组中除第一个元素之外的所有元素。

**方法 1:使用 for 循环**
在这个方法中，我们将使用一个 for [循环](https://www.geeksforgeeks.org/javascript-for-loop/)来抓取除第一个元素之外的所有元素。我们知道，在数组中，第一个元素出现在索引“0”处。我们将运行一个从 1 到数组*的循环。长度*并将剩余的元素保存到另一个数组中。

**示例:**

## java 描述语言

```
<script>
    //Javascript program to find all
    //element of an array except first

    //function which takes an array as argument
    const print = (arr) => {

        //creating a dummy array to store result
        const find = []

        //a counter for adding result
        let k = 0

        for (let i = 1; i < arr.length; i++) {
            find[k] = arr[i]
            k++
        }
        //returning resultant array
        return find
    }

    //input array
    const arr = [1, 2, 3, 4, 5]

    //printing the result
    console.log(print(arr))
</script>
```

**输出:**

```
[ 2, 3, 4, 5 ]
```

**方法二:使用切片()方法**

**切片()**是返回数组切片的方法。它需要两个参数，开始和结束索引。

**示例:**

## java 描述语言

```
<script>
    //Javascript program to find all
    //element of array except first

    //function which takes an array as argument
    const print = (arr) => {

        //returning resultant array
        return arr.slice(1)
    }

    //input array
    const arr = [10, 20, 30, 40, 50]
    //printing the result
    console.log(print(arr))
</script>
```

**输出:**

```
[20, 30, 40, 50]
```