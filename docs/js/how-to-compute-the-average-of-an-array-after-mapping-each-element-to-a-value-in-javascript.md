# 在 JavaScript 中将每个元素映射到一个值后，如何计算一个数组的平均值？

> 原文:[https://www . geesforgeks . org/如何计算将每个元素映射到 javascript 中的值后的数组平均值/](https://www.geeksforgeeks.org/how-to-compute-the-average-of-an-array-after-mapping-each-element-to-a-value-in-javascript/)

给定一个数组，任务是在将每个元素映射到一个值之后计算数组的平均值。

```
Input : arr=[2, 3, 5, 6, 7]
Output: 4.6
Explanation : (2+3+5+6+7)/5 = 4.6 

Input : [5,7,2,7,8,3,9,3]
Output: 5.5
Explanation : (5+7+2+7+8+3+9+3)/8 = 5.5 
```

**接近 1:**

*   使用 [foreach()](https://www.geeksforgeeks.org/javascript-array-foreach-method/) 循环迭代数组元素。
*   将每个元素的总和存储在变量中。
*   所有元素的平均值将是 sum/length，其中 length 是给定数组的大小。

**Index.js**

## java 描述语言

```
<script>
  arr = [2, 3, 5, 6, 7];

  // Function to calculate the average of numbers
  function avg(arr) {
    var sum = 0;

    // Iterate the elements of the array
    arr.forEach(function (item, idx) {
      sum += item;
    });

    // Returning the average of the numbers
    return sum / arr.length;
  }

  console.log(avg(arr));
</script>
```

**输出:**

```
4.6
```

**方法 2:**

*   使用 for 循环迭代数组的数字
*   使用[ParseInt()](https://www.geeksforgeeks.org/what-is-the-difference-between-parseint-and-number/) 函数解析十进制格式的数字。
*   将数字的总和存储在变量中。
*   所有元素的平均值将是 sum/length，其中 length 是给定数组的大小。

**Index.js**

## java 描述语言

```
<script>
  arr = [2, 3, 5, 6, 7];
  var sum = 0;

  // Iterating the elements of the loop
  for (var i = 0; i < arr.length; i++) {

    // Store the sum of all numbers
    sum += parseInt(arr[i], 10);
  }

  // Taking the average
  var avg = sum / arr.length;

  console.log(avg);
</script>
```

**输出:**

```
 4.6
```

**进场 3:使用** [**减少()**](https://www.geeksforgeeks.org/javascript-typedarray-reduce-with-examples/#:~:text=reduce()%20is%20an%20inbuilt,right%20into%20a%20single%20value.&text=previousValue%3A%20It%20is%20the%20previously,being%20processed%20in%20the%20typedArray.) **功能**

*   在这种方法中，我们减少，即在原始数组中用它们的和替换数组的两个数字。
*   函数的作用是:返回一个值，即数组中所有数字的总和。
*   将返回值存储在变量中(使用 sum 变量)。
*   所有元素的平均值将是 sum/length，其中 length 是给定数组的大小。

**Index.js**

## java 描述语言

```
<script>
  var arr = [1, 2, 3, 4];
  // Callback function calculating
  // the sum of two numbers
  function check(a, b) {
    return a + b;
  }

  // Reducing the numbers of the array
  var sum = arr.reduce(check);

  // Calculating the average of the numbers
  var avg = sum / arr.length;

  console.log(avg);
</script>
```

**输出:**

```
2.5
```