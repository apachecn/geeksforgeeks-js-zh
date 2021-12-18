# 如何在 JavaScript 中迭代回调 n 次？

> 原文:[https://www . geeksforgeeks . org/如何迭代回调 n 次 javascript/](https://www.geeksforgeeks.org/how-to-iterate-over-a-callback-n-times-in-javascript/)

给定一个回调函数，我们必须迭代回调 n 次。回调是作为参数传递的函数。为了迭代回调函数，我们必须运行回调函数 n 次。

**方法 1:** 我们用递归迭代 n 次回调函数。

*   首先创建以 n 为参数的回调函数因子。
*   因子函数生成 n 长度的模式。
*   创建带有回调函数和 n 的测试函数。
*   测试函数检查 n 的值是否等于 0。
*   如果 n 为 0，则返回终止测试函数，否则调用打印模式的回调函数。

**示例:**

## java 描述语言

```
<script>
  // callback function that print pattern
  function factor(n) {
    // base case for recursion
    if (n <= 1) {
      console.log("0" + n);
      return;
    }
    // string to store patterns
    let str = "";
    // loop for generate patter
    for (let i = 1; i <= n; i++) {
      str += `0${i} `;
    }
    // printing patterns
    console.log(str);

    // recursion call with decrement by 1
    return factor(n - 1);
  }

  // function to run callback function
  function test(n, callback) {
    if (n == 0) {
      console.log("please provide value n greater than 0");
      return;
    }

    let k = n;
    //calling callback function
    callback(k);
  }

  // initialising test number
  let t_number = 4;
  // calling main function to call callback function
  test(t_number, factor);
</script>
```

**输出:**

```
01 02 03 04
01 02 03
01 02
01
```

**方法 2:** 我们使用循环语句迭代回调。

*   首先我们创建回调函数因子，它生成数的阶乘。
*   用参数 n 和回调函数创建测试函数。
*   如果 n 值无效，请检查该值；如果不继续，请终止。
*   为范围为 n 的循环创建。
*   在每个循环上调用回调函数，该函数打印每个数字的阶乘。

**示例:**

## java 描述语言

```
<script>
  // call back function thar return factorial
  function factor(number) {
    let j = 1;
    // loop that generate factorial of number
    for (let i = 1; i <= number; i++) {
      j *= i;
    }
    // printing value of factorial
    console.log(`factorial of ${number} is `);
    console.log(j);
  }

  // function that iterate over callback function
  function test(n, callback) {
    if (n <= 0) {
      console.log("invalide number");
      return;
    }
    let k = n;
    // iterating over callback function with for loop
    for (let i = k; i >= 1; i--) callback(i);
  }

  // initialising test variable
  let t_umber = 5;
  // main function calling
  test(t_umber, factor);
</script>
```

**输出:**

```
factorial of 5 is 120
factorial of 4 is 24
factorial of 3 is 6
factorial of 2 is 2 
factorial of 1 is 1
```