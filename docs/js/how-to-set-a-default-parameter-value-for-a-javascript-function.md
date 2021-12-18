# 如何设置 JavaScript 函数的默认参数值？

> 原文:[https://www . geesforgeks . org/如何为 javascript 函数设置默认参数值/](https://www.geeksforgeeks.org/how-to-set-a-default-parameter-value-for-a-javascript-function/)

让我们先来看看一个问题，然后我们再来看看函数参数的默认值是如何解决这个问题的。
我们先创建一个简单的函数。
**例 1:**

```
<script>
    /* This function is simply going to
        multiply two numbers that are passed in*/
    var multiplyIt = function(num1, num2) {

        // So we are returning num1 times num2
        return (num1 * num2);
    };

    /* Now lets see what happens if we call the 
    above function without passing anything in*/
    console.log(multiplyIt()); 
</script>
```

该语句在某些语言中会产生错误，但在 JavaScript 中，这是允许的。所以基本上，这个函数会用 undefined 乘以 undefined。

**输出:**

```
NaN 
```

因为函数试图将两个不是数字的东西相乘。

传统上，您会在函数中传递值，但是建立默认值要简单得多，并且您可以将其作为函数中参数的一部分。
**例 2:**

```
<script>

    //These values will only be taken if a value is not passed in
    var multiplyIt = function(num1 = 2, num2 = 5) 
        {
            return (num1 * num2);
        };
    console.log(multiplyIt()); 
</script>
```

**输出:**

```
10
```

**例 3:** 现在试着输入值 10 和 100。

```
<script>

    //In this case, these values will not be considered
    var multiplyIt = function(num1 = 2, num2 = 5) 
        {
            return (num1 * num2);
        };
    console.log(multiplyIt(10, 100));

</script>
```

**输出:**

```
1000
```