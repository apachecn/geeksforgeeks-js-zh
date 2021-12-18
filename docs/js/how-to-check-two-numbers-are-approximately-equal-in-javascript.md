# 如何在 JavaScript 中检查两个数是否近似相等？

> 原文:[https://www . geesforgeks . org/如何检查两个数字在 javascript 中是否大致相等/](https://www.geeksforgeeks.org/how-to-check-two-numbers-are-approximately-equal-in-javascript/)

给定两个数字，任务是检查给定的数字是否大致相等。如果两个数字大致相同，则打印为真，否则打印为假。

**示例:**

```
Input:  num1 = 10.3
        num2 = 10

Output: true
```

**方法:**要检查数字是否大致相同，首先要决定ε值。ε是两个数字之间的最大差值，如果两个数字的差值小于或等于ε，则两个数字大致相等。所以首先我们创建一个名为**的函数来检查取三个参数 num1，num2 和ε。现在检查 num1 和 num2 的绝对差值是否小于ε。**

**例 1:**

## java 描述语言

```
<script>
const checkApprox = (num1, num2, epsilon) => {

  // Calculating the absolute difference
  // and compare with epsilon
  return Math.abs(num1 - num2) < epsilon;
}

console.log(checkApprox(10.003, 10.001, 0.005));
</script>
```

**输出:**

```
true
```

**例 2:**

## java 描述语言

```
<script>
const checkApprox = (num1, num2, epsilon = 0.004) => {
  return Math.abs(num1 - num2) < epsilon;
}

console.log(checkApprox(Math.PI / 2.0, 1.5708));
</script>
```

**输出:**

```
true
```

**例 3:**

## java 描述语言

```
<script>
const checkApprox = (num1, num2, epsilon = 0.004) => {
  return Math.abs(num1 - num2) < epsilon;
}

console.log(checkApprox(0.003, 0.03));
</script>
```

**输出:**

```
false
```