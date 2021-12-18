# 如何用 JavaScript 得到一组数字的标准差？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 获取数字数组的标准偏差/](https://www.geeksforgeeks.org/how-to-get-the-standard-deviation-of-an-array-of-numbers-using-javascript/)

给定一个数组，任务是计算它的标准差。

**例**:

```
Input:  [1, 2, 3, 4, 5]
Output: 1.4142135623730951

Input:  [23, 4, 6, 457, 65, 7, 45, 8]
Output: 145.13565852332775
```

详见[均值、方差、标准差](https://www.geeksforgeeks.org/mathematics-mean-variance-and-standard-deviation/)。

> 平均值是元素的平均值。其中 0 <= i < n
> 
> arr 平均值[0..n-1] = ∑(arr[i]) / n
> 
> 方差是平均值的平方差除以若干元素的总和。
> 
> 方差=∑(arr[I]–均值)2 / n
> 
> 标准差是方差的平方根。
> 
> 标准偏差=方差^ 1/2

**方法:**要计算标准偏差，我们首先计算平均值，然后计算方差，然后计算偏差。为了计算平均值，我们使用 [Array.reduce()](https://www.geeksforgeeks.org/javascript-array-reduce-method/) 方法，计算所有数组项的和，然后用数组的长度来划分数组。

为了计算方差，我们使用 [map()](https://www.geeksforgeeks.org/map-in-javascript/) 方法，通过给每个数组项赋值(value–mean)^ 2 来变异数组，然后我们计算数组的和，然后我们用数组的长度除以和。为了计算标准差，我们计算数组的平方根。

**示例:**

## java 描述语言

```
<script>
// Javascript program to calculate the standered deviation of an array
function dev(arr){
  // Creating the mean with Array.reduce
  let mean = arr.reduce((acc, curr)=>{
    return acc + curr
  }, 0) / arr.length;

  // Assigning (value - mean) ^ 2 to every array item
  arr = arr.map((k)=>{
    return (k - mean) ** 2
  })

  // Calculating the sum of updated array
 let sum = arr.reduce((acc, curr)=> acc + curr, 0);

 // Calculating the variance
 let variance = sum / arr.length

 // Returning the Standered deviation
 return Math.sqrt(sum / arr.length)
}

console.log(dev([1, 2, 3, 4, 5]))
console.log(dev([23, 4, 6, 457, 65, 7, 45, 8]))
</script>
```

**输出:**

```
1.4142135623730951
145.13565852332775
```