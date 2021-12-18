# 如何在 JavaScript 中否定一个谓词函数？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中否定谓词函数/](https://www.geeksforgeeks.org/how-to-negate-a-predicate-function-in-javascript/)

在本文中，我们将看到如何否定 JavaScript 中的谓词函数。谓词函数是检查条件并基于参数返回*真*和*假*的函数。我们的任务是得到谓词函数的反义词。

我们按照下面的方法得到想要的结果。

**方法 1:** 我们的谓词功能是检查奇数和偶数。如果数字是 2 的模，它返回 1，那么它是奇数，否则它是偶数。检查参数条件时否定逻辑。

**示例:**

## java 描述语言

```
<script>
  // Predicate function check odd
  function isOdd(number) {
    return number % 2 == 1;
  }
  // negation of isOdd function
  function isNotOdd(number) {
    return number % 2 !== 1;
  }
  // Predicate function check Even
  function isEven(number) {
    return number % 2 == 0;
  }
  // negation of isEven function
  function isNotEven(number) {
    return number % 2 !== 0;
  }

  // Outputs: true
  console.log(isOdd(5));

  // Outputs: true
  console.log(isNotOdd(2));

  // Output: false
  console.log(isEven(3));

  // Output> false
  console.log(isNotEven(4));
</script>
```

**输出:**

```
true
true 
false
false
```

**方法 2:** 上述方法的问题在于，我们在每次否定时都会对逻辑进行硬编码。在否定条件下，我们可能有更多的机会犯错。更有效的是通过检查条件来否定谓词函数。

**示例:**

## java 描述语言

```
<script>
  // Predicate function check odd
  function isOdd(number) {
    return number % 2 == 1;
  }
  // negation of isOdd function
  function isNotOdd(number) {
    return !isOdd(number);
  }
  // Predicate function check Even
  function isEven(number) {
    return number % 2 == 0;
  }
  // negation of isEven function
  function isNotEven(number) {
    return !isEven(number);
  }

  // Outputs: true
  console.log(isOdd(5));

  // Outputs: true
  console.log(isNotOdd(10));

  // Output: false
  console.log(isEven(3));

  // Output> false
  console.log(isNotEven(4));
</script>
```

**输出:**

```
true 
true 
false
false
```

**方法 3:** 在前面的方法中，我们正在否定所有谓词函数的函数。但是如果我们创建一个否定所有谓词函数的函数，我们的解决方案会更有效。我们制作谓词函数，并将否定函数与所有谓词函数绑定。

**示例:**

## java 描述语言

```
<script>
  // Predicate function check odd
  function isOdd(number) {
    return number % 2 == 1;
  }

  // Predicate function check Even
  function isEven(number) {
    return number % 2 == 0;
  }

  // function that negate all function
  function negate(pre) {
    return function (number) {
      return !pre(number);
    };
  }
  // Wrapping predicate function to negate function
  var isNotOdd = negate(isOdd);
  var isNotEven = negate(isEven);

  // Outputs: true
  console.log(isOdd(5));

  // Outputs: true
  console.log(isNotOdd(10));

  // Output: false
  console.log(isEven(3));

  // Output: false
  console.log(isNotEven(4));
</script>
```

**输出:**

```
true 
true 
false 
false
```