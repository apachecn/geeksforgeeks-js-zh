# 用 JavaScript 解释 MUL()函数？

> 原文:[https://www . geesforgeks . org/explain-the-mul-function-in-JavaScript/](https://www.geeksforgeeks.org/explain-the-mul-function-in-javascript/)

MUL 函数是乘法函数的一个缩影。在这个函数中，我们调用需要一个参数作为第一个数字的函数，这个函数调用另一个需要另一个参数的函数，这一步继续。

第一个函数的参数是 x，第二个函数的参数是 y，第三个是 z，所以返回值将是 xyz。

**语法:**

```
function mul(x) {
  return function (y) {
    return function (z) {
      return x * y * z;
    };
  };
}
```

**示例:**下面的示例说明了 JavaScript 中的 MUL()函数。

## Javascript

```
<script>
function mul(x) {
  return function(y) {
    return function(z) {
      return x*y*z;
    };
  }
}

console.log(mul(2)(3)(5));
console.log(mul(2)(3)(4));
</script>
```

**输出:**

```
30
24
```