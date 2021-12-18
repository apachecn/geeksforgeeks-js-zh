# 如何创建一个函数，该函数调用提供的函数，其参数在 JavaScript 中转换？

> 原文:[https://www . geeksforgeeks . org/如何创建一个函数，该函数调用提供的带有参数的 javascript 转换函数/](https://www.geeksforgeeks.org/how-to-create-a-function-that-invokes-the-provided-function-with-its-arguments-transformed-in-javascript/)

在编程中，函数用于减少重复编写同一代码实例的工作量。在本文中，让我们看看如何创建一个函数，该函数调用所提供的函数，其参数用 JavaScript 进行转换。

在本文中，函数转换器调用带有参数的函数缩放，其中函数缩放通过将其参数缩放到一次、两次和三次来缩放参数，从而转换给定的参数。

**语法:**

**第一路:**

```
function function_name ( argument1, argument2,....){
  instruction1;
  instruction2;
  ....
 return parameters;
}
```

**第二路:**

```
var function_name = function ( argument1, argument2,....){
   instruction1;
   instruction2;
   ....
 return parameters;
}
```

**例:**

## java 描述语言

```
<script>
  function scaling(num1, num2, num3)
  {
    return [1 * num1, 2 * num2, 3 * num3];
  }
  function transformer(num1, num2, num3)
  {
      var tran=scaling(num1, num2, num3);
      console.log(tran);

  }
  var num1=5;
  var num2=5;
  var num3=5;
  transformer(num1, num2, num3);
</script>
```

**输出:**输出下面是转换后的参数数组。

```
[5, 10, 15]
```

**示例:**通过调用平方函数将参数转换为它们的平方。

## java 描述语言

```
<script>
  function square(num1, num2, num3) {
      return [num1 * num1, num2 * num2, num3 * num3];
  }
  function transformer(num1, num2, num3) {
      var tran = square(num1, num2, num3);
      console.log(tran);

  }
  var num1 = 5;
  var num2 = 10;
  var num3 = 15;
  transformer(num1, num2, num3);
</script>
```

**Output:**

```
[25, 100, 225]
```