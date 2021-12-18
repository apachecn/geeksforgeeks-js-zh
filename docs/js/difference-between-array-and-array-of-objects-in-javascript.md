# JavaScript 中数组和对象数组的区别

> 原文:[https://www . geesforgeks . org/JavaScript 中对象数组和数组之间的区别/](https://www.geeksforgeeks.org/difference-between-array-and-array-of-objects-in-javascript/)

在本文中，我们将看到 JavaScript 中数组和对象数组之间的区别。

**1。数组:**一个**数组**是一组数据和一个数据结构，存储在一系列**内存**位置中。通过调用索引号，如 0、1、2、3、…，可以访问数组的元素。数组可以存储数据类型，如**整数、浮点、字符串和布尔**所有**原始数据类型**都可以存储在数组中。

**例:**

## Javascript

```
<script>
    var myArr = [1, 2, 3, 4, 5];

    // Iterating through loop
    for (var i = 0; i < myArr.length; i++) {
        console.log(myArr[i]);
    }

    // Pop an element from array
    myArr.pop();
    console.log("after using pop()" + myArr);
</script>
```