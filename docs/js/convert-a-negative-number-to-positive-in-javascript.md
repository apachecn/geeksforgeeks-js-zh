# 在 JavaScript 中把负数转换为正数

> 原文:[https://www . geesforgeks . org/convert-a-负数-正数-in-javascript/](https://www.geeksforgeeks.org/convert-a-negative-number-to-positive-in-javascript/)

我们可以通过下面描述的方法在 javascript 中将负数转换为正数。

**方法 1:** 这是一个通用的方法，首先我们会检查这个数字是已经是正数还是负数，如果这个数字是负数，那么我们会将这个数字乘以 **-1** 使其为正数。

**语法:**

```
if (a < 0) {
    a = a * -1;
}

```

**示例:**下面是上述方法的实现:

```
<script>
    // Javascript script 
    // to convert negative number
    // to positive number

    // Function to convert
    // given number to 
    // positive number
    function convert_positive(a) {
        // Check the number is negative
        if (a < 0) {
            // Multiply number with -1
            // to make it positive
            a = a * -1;
        }
        // Return the positive number
        return a;
    }

//Driver code
var n = -10;
var m = 5;

// Call function
n = convert_positive(n);

// Print result
document.write(n + "<br>");

// Call function
m = convert_positive(m);

// Print result
document.write(m + "<br>"); 
</script>
```

**输出:**

```
10
5

```

**方法二:**在此方法中我们将使用 [Math.abs()](https://www.geeksforgeeks.org/javascript-math-abs-function/) 函数将负数转换为正数。

**语法:**

```
Math.abs(value)
```

**示例:**下面是上述方法的实现:

```
<script>
    // Javascript script 
    // to convert negative number
    // to positive number

    //Driver code
    var n = -30;
    var m = 15;

    // Using Math.abs() function
    n = Math.abs(n);

    // Print result
    document.write(n + "<br>");

    // Using Math.abs() function
    m = Math.abs(m);

    // Print result
    document.write(m + "<br>");
</script>                                    
```

**输出:**

```
30
15

```