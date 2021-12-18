# 在 JavaScript 中执行速度最快的函数数组中，如何获取函数的索引？

> 原文:[https://www . geesforgeks . org/如何获取函数数组中函数的索引——执行速度最快的 javascript/](https://www.geeksforgeeks.org/how-to-get-the-index-of-the-function-in-an-array-of-functions-which-executed-the-fastest-in-javascript/)

在这个例子中，我们将学习如何在 JavaScript 中执行最快的函数数组中获取函数的索引。

**示例:**

```
Input: fun[] = [ hello, hello1, hello2 ]
Output: index of fastest is 0.

Explanation: Function hello execute fastest in all functions.

Input: fun[] = [ while1, while2, while3 ]
Output: index of fastest function is 2 
```

**方法:**解决问题必须遵循以下步骤:

*   我们将首先迭代给定的数组。
*   我们将找到每个函数花费的时间，并将其存储在一个不同的数组中，该数组的索引值与函数索引相同。通过使用 **performance.now()** 方法获得时间差，可以找到所花费的时间。
*   最后，我们通过使用 **Math.min()** 方法获取数组的最小值来打印最小索引。

下面的例子演示了这种方法。

**例 1:**

## java 描述语言

```
<script>
  // 1st function
  function hello() {
    var s = "";
    var ans = ["The", " hello function ", "takes "];
    for (var i = 0; i < 3; i++) s += ans[i];
    console.log(s);
  }

  // 2nd function
  function hello1() {
    var s = "";
    var ans = ["The hello1 function", " takes "];
    for (var i = 0; i < 2; i++) s += ans[i];
    console.log(s);
  }

  // 3rd function
  function hello2() {
    var ans = "The hello2 function takes ";
    for (var i = 0; i < 1; i++) console.log(ans);
  }

  // Function to check time required by each function
  function findTime(f) {

    // Storing initial time in start
    var start = performance.now();

    // Calling the function
    f();

    // Storing time after running the function
    var end = performance.now();

    // Return time taken by function
    return end - start;
  }

  function findMinTime() {

    // Initializing array of functions
    var fun = [hello, hello1, hello2];

    // Initialising array of time taken by function
    var ans = [];

    // Iterating over all the functions and
    // storing time taken by them
    for (var i = 0; i < 3; i++) {
      var n = findTime(fun[i]);
      ans[i] = n;
      console.log(ans[i]);
    }

    // Finding the minimum time in array
    var answer = Math.min.apply(null, ans);
    c = ans.indexOf(answer);

    // Return index of fastest array
    return c;
  }

  var minTime = findMinTime();
  console.log("Index of fastest function:", minTime);
</script>
```

**输出:**

```
The hello function takes
5.8547000009566545
The hello1 function takes
0.2459999993443489
The hello2 function takes
0.19830000028014183
Index of fastest function
2
```

**例 2:**

## java 描述语言

```
<script>
  // 1st function
  function fac(n) {
    let fact = 1;
    for (let i = 1; i < 4; i++)
      fact *= i;
    console.log("Factorial of 4 is:", fact);
  }

  // 2nd function
  function fibo() {
    let fab = 1;
    let j = 1;
    for (let i = 2; i < 6; i++) {
      let temp = fab;
      fab += j;
      j = temp;
    }
    console.log("6th fibonacci no is:", fab);
  }

  // 3rd function
  function binpow() {
    let j = 2;
    let k = 22;
    for (let i = 0; i < k; i++)
      j = ((j * j) % 1e9) + 7;
    console.log(
      "Power 2 to 22 mod 1e9+7 is:", j
    );
  }

  // Function to check time required
  // by each function
  function findTime(f) {

    // Storing initial time in start
    var start = performance.now();

    // Calling the function
    f();

    // Storing time after running the function
    var end = performance.now();

    // Return time taken by function
    return end - start;
  }

  function findMinTime() {

    // Initializing array of functions
    var fun = [fac, fibo, binpow];

    // Initialising array of time
    // taken by function
    var ans = [];

    // Iterating over all the functions
    // and storing time taken by them
    for (var i = 0; i < 3; i++) {
      var n = findTime(fun[i]);
      ans[i] = n;
      console.log(ans[i]);
    }

    // Finding the minimum time in array
    var answer = Math.min.apply(null, ans);
    c = ans.indexOf(answer);

    // Return index of fastest array
    return c;
  }

  var minTime = findMinTime();
  console.log("Index of fastest function:",
              minTime);
</script>
```

**输出:**

```
Factorial of 4 is: 6
7.554999999701977
6th fibonacci no is: 8
0.22690000012516975
Power 2 to 22 mod 1e9+7 is: 221047735
0.25120000168681145
Index of fastest function: 1
```