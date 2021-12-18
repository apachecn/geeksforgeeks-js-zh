# 如何创建一个函数，用 JavaScript 接收的参数调用每个提供的函数？

> 原文:[https://www . geeksforgeeks . org/如何创建一个函数，该函数使用 javascript 调用它接收的每个函数提供的参数/](https://www.geeksforgeeks.org/how-to-create-a-function-that-invokes-each-provided-function-with-the-arguments-it-receives-using-javascript/)

在本文中，我们将看到如何创建一个函数，该函数使用 JavaScript 接收的参数调用每个提供的函数。

它有助于减少反复创建相同代码实例的工作量。在本文中，让我们看看如何创建一个函数，该函数使用它接收的参数调用每个提供的函数，并在 JavaScript 中返回值。

可以通过两种方式定义函数:

**语法:**

```
function <function_name>(arg_1,arg_2,...)
{
   <set of instructions>;
}

//INVOKER
var returned_value= function_name(arguments);
```

运筹学

```
var function_name = function(arg_1,arg_2,...)
{
  <set of instructions>;
}

// INVOKER
var returned_value = function_name(arguments);
```

下面是帮助我们轻松理解问题的例子。

**示例 1:** 用于分隔数组中的偶数和奇数。**查找偶数**和**查找奇数**函数通过**分离奇数**函数获取相同的参数，并在**分离奇数**函数中调用。

## java 描述语言

```
<script>
  // Defined array
  var ar =
      [1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8];
  function findEven(ar){
    var res1 = [];
    for (let geek = 0; geek < ar.length; geek++) {
        if (ar[geek] % 2 === 0) {
            res1.push(ar[geek]);
        }
    }
    return res1;
  }

  function findOdd(ar){
    var res2 = [];
    for (let geek = 0; geek < ar.length; geek++) {
        if (ar[geek] % 2 === 1) {
            res2.push(ar[geek]);
        }
    }
    return res2;
  }

  function segregateEvenOdd(ar) {

    // Invoking findEven and findOdd functions
    var even = findEven(ar);
    var odd = findOdd(ar);
    console.log("Before Segregation: ");
    console.log(ar);
    console.log("After Segregation: ");
    console.log("Even integers: " + even);
    console.log("Odd integers: " + odd);
  }

  // Invoker
  segregateEvenOdd(ar);
</script>
```

**输出:**

```
"Before Segregation: "
[1, 2, 2, 3, 4, 5, 6, 6, 7, 8, 8, 8]
"After Segregation: "
"Even integers: 2,2,4,6,6,8,8,8"
"Odd integers: 1,3,5,7"
```

**例 2:** 求数组中最小值和最大值的函数。 **findMin** 和 **findMax** 函数采用与 **FindMinMax** 函数相同的参数，并在 **FindMinMax** 函数中调用。

## java 描述语言

```
<script>
  // Defined array
  var ar = [20, 30, 40, 50, 60, -20, -40, 90, 100];
  function findMin(ar) {
      var res1 = Number.MAX_VALUE;;
      for (let geek = 0; geek < ar.length; geek++) {
          if (ar[geek] < res1) {
              res1 = ar[geek];
          }
      }
      return res1;
  }
  function findMax(ar) {
      var res2 = Number.MIN_VALUE;
      for (let geek = 0; geek < ar.length; geek++) {
          if (ar[geek] > res2) {
              res2 = ar[geek];
          }
      }
      return res2;
  }

  function FindMinMax(ar) {
      // Invoking findMin and findMax functions
      var min = findMin(ar);
      var max = findMax(ar);
      console.log("Given array : ");
      console.log(ar);
      console.log("Minimum in the array: " + min);
      console.log("Maximum in the array: " + max);

  }
  // Invoker
  FindMinMax(ar);
</script>
```

**输出:**

```
"Given array : "
[20, 30, 40, 50, 60, -20, -40, 90, 100]
"Minimum in the array: -40"
"Maximum in the array: 100"
```