# 如何在 JavaScript 中深度展平一个数组？

> 原文:[https://www . geesforgeks . org/如何深度展平 javascript 中的数组/](https://www.geeksforgeeks.org/how-to-deep-flatten-an-array-in-javascript/)

在本文中，我们将学习如何在 JavaScript 中深度展平数组。数组的展平是一个合并给定数组中一组嵌套数组的过程。深度展平意味着阵列将完全展平。

**示例:**

```
Input: [1,2,3,4,5,[6,[7,8,9]]] 
Output: [1,2,3,4,5,6,7,8,9]
```

这可以使用以下方法来完成。

**方法 1:** 使用 JavaScript 中的 **[flat()](https://www.geeksforgeeks.org/javascript-array-flat-method/)** 方法。此方法合并数组中存在的所有嵌套数组。此方法采用参数深度，它是一个整数，指定嵌套数组需要展平的深度。深度值可以指定为 ***无穷大*** 来完全展平阵列。此参数的默认值为 1。

**示例:**

## java 描述语言

```
<script>
  const arr = [1,2,3,4,5,[6,[7,8,9]]];

  // Setting the depth value to
  // Infinity to deep flatten the array
  const flattened = arr.flat(Infinity);
  console.log(flattened)
</script>
```

**输出:**

```
[1,2,3,4,5,6,7,8,9]
```

**方法 2:** 使用下划线库的 **[展平()](https://www.geeksforgeeks.org/underscore-js-_-flatten-with-examples/)** 方法，可以将数组展平到任意深度。它将数组作为参数，并返回展平的数组。如果没有深度参数传递给方法，数组将被完全展平。

**示例:**

## java 描述语言

```
const underscore = require('underscore');
const arr = [1,2,3,4,5,[6,[7,8,9]]];

// Using the flatten() method without
// depth parameter to deep flatten
// the array
const flattened_arr = underscore.flatten(arr);
console.log(flattened_arr);
```

**输出:**

```
[1,2,3,4,5,6,7,8,9]
```

**方法 3:** 使用洛达什库的**[flappendeep()](https://www.geeksforgeeks.org/lodash-_-flattendeep-and-_-flattendepth-method/)**方法。这个方法用于递归展平一个数组。它以数组作为参数，并返回深度展平数组。

**示例:**

## java 描述语言

```
const lodash = require('lodash');
const arr = [1,2,3,4,5,[6,[7,8,9]]];

// Using the flattenDeep() method
// to deep flatten the array
const flattened_arr = lodash.flattenDeep(arr);
console.log(flattened_arr);
```

**输出:**

```
[1,2,3,4,5,6,7,8,9]
```