# 如何用 JavaScript 一次找到两个给定数组中任意一个存在的每个元素？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 找到两个给定数组中任何一个数组中存在的每个元素/](https://www.geeksforgeeks.org/how-to-find-every-element-that-exists-in-any-of-two-given-arrays-once-using-javascript/)

在本文中，我们将学习如何找到存在于给定的两个数组中的每个元素。

**方法 1:使用套装**

一个[集合](https://www.geeksforgeeks.org/sets-in-javascript/)是唯一的项目集合，即没有可以重复的元素。我们将两个数组的所有元素添加到集合中，然后返回集合。

**示例:**

> const arr1 = [1，2，3，4，5]
> const arr2 = [1，2，3，4，5，6]
> 
> 结果= [1，2，3，4，5，6]

**代码示例:**

## java 描述语言

```
<script>

    // Javascript program to find all element
    // present in any of two given arrays

    // Function which takes an array as argument
    const print = (arr1,arr2) => {

        // Creating a set with elements of arr1
        const set = new Set(arr1)

        // Adding elements of arr2
        arr2.forEach(element => {
            set.add(element)
        });

        // Returning resultant array
        return set
    }

    // Input array
    const arr1 = [10, 20, 30, 40, 50]
    const arr2 = [10,20,34,32,11]

    // Printing the result
    console.log(print(arr1,arr2))
</script>
```

**输出:**

```
{10, 20, 30, 40, 50, 34, 32, 11}
```

**方法二:使用循环**

在这种方法中，我们将选择一个数组，然后在第二个数组上运行一个循环，并检查第一个数组中是否存在该数组的元素。如果一个元素已经存在，我们跳过，否则我们将把它添加到第一个数组中。

**代码示例:**

## java 描述语言

```
<script>
    // Javascript program to find all element
    // present in any of two given arrays

    // Function which takes an array as argument
    const print = (arr, arr2) => {

        // A counter for adding element
        let k = arr.length

        // Checking every element and
        // adding required element
        arr2.forEach(element => {
            if (arr.indexOf(element) == -1) {
                arr[k] = element
                k++
            }
        });

        // Returning resultant array
        return arr
    }

    // Input array
    const arr1 = [1, 2, 3, 4, 5]
    const arr2 = [1, 2, 3, 4]

    // Printing the result
    console.log(print(arr1, arr2))
</script>
```

**输出:**

```
[1, 2, 3, 4, 5]
```