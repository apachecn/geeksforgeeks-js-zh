# 如何在 JavaScript 中计算两个整数 n 和 k 的二项式系数？

> 原文:[https://www . geeksforgeeks . org/如何在 javascript 中计算二项整数系数 n 和 k/](https://www.geeksforgeeks.org/how-to-evaluate-binomial-coefficient-of-two-integers-n-and-k-in-javascript/)

以下是[二项式系数的常用定义。](http://en.wikipedia.org/wiki/Binomial_coefficient)

一个二项式系数 C(n，k)可以定义为 x^k 系数在(1 + x)^n.二项式系数 C(n，k)的展开式中也给出了数种方式，不考虑顺序，即 k 个对象可以从 n 个对象中选择更正式地说，n 个元素集合的 k 个元素子集(或 k 个组合)的数量。

**问题陈述:**写一个函数，取两个参数 n 和 k，返回二项式系数 C(n，k)的值。例如，对于 n = 4 和 k = 2，您的函数应该返回 6，对于 **n = 5** 和 **k = 2** ，它应该返回 **10** 。

**方法:**下面是创建一个返回两个整数的二项式系数的函数需要遵循的步骤。

*   Create a function for parameters **n** and **k** .
*   Now check whether **n** and **k** are numbers. If either or both of them are not numbers, **nan is returned.**
*   Now check whether **k** is less than **0** or **k** is greater than n. If one of the statements is true, return **0** .
*   Now check whether **k** is equal to **1** or **k** is equal to **n** . If one of the statements is true, return **1** .
*   Now check whether **k** is equal to **1** or **k** is equal to **(n-1).** If one of the statements is true, return **n** .
*   Now write logic to get binomial coefficient.

**例:**

## Javascript

```
<script>
  function binomialCoefficient (n, k){

    // Checkuing if n and k are integer
    if(Number.isNaN(n) || Number.isNaN(k)){
      return NaN;
    }

    if(k < 0 || k > n){
      return 0
    }

    if(k === 0 || k === n){
      return 1
    }

    if(k === 1 || k === n - 1){
      return n
    }

    let res = n;
    for(let i = 2; i <= k; i++){
      res *= (n - i + 1) / i;
    }

    return Math.round(res);
  }

  console.log(binomialCoefficient(10, 2))
</script>
```

**输出:**

```
45
```