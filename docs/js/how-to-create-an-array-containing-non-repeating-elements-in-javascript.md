# 如何在 JavaScript 中创建包含非重复元素的数组？

> 原文:[https://www . geesforgeks . org/如何创建包含非重复元素的数组 javascript/](https://www.geeksforgeeks.org/how-to-create-an-array-containing-non-repeating-elements-in-javascript/)

以下是生成包含**非重复随机数**的 **n** 个数组的两种方法。

1.  Loop while using and include () function.
2.  Use the set and check its dimensions.

**使用 do-while 循环和 includes()函数:**这里，includes()函数检查数组中是否存在元素。

**档案名称:index . js**

## 【JavaScript】

```
// You can take this value from user
const n = 5

// Initial empty array
const arr = [];

// Null check
if (n == 0) {
    console.log(null)
}

do {
    // Generating random number
    const randomNumber = Math
        .floor(Math.random() * 100) + 1

    // Pushing into the array only 
    // if the array does not contain it
    if (!arr.includes(randomNumber)) {
        arr.push(randomNumber);
    }

} while (arr.length < n);

// Printing the array elements
console.log(arr)
```