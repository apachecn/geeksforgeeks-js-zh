# 如何用 JavaScript 将一个值转换成安全的整数？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将值转换为安全整数/](https://www.geeksforgeeks.org/how-to-convert-a-value-to-a-safe-integer-using-javascript/)

在本文中，我们将学习如何使用 JavaScript 将值转换为安全的整数。我们已经给出了一个数字，我们必须用 JavaScript 把它转换成一个安全的整数。安全整数是介于**-(2<sup>53</sup>–1)**和**(2<sup>53</sup>–1)**之间的整数。

**方法:**首先，我们使用 JavaScript 中的提示进行输入。并将输入存储在一个名为 input 的变量中。现在我们做两个变量，一个叫做mini，包含输入的最小值和[**MAX _ SAFE _ INTEGER**](https://www.geeksforgeeks.org/javascript-number-max_safe_integer-constant/)**【2】<sup>53</sup>-1】**，另一个叫做 maxi，包含 mini 和[**MIN _ SAFE _ INTEGER**](https://www.geeksforgeeks.org/javascript-number-min_safe_integer-constant/)**【-(2<sup>53</sup>-1】】**。现在我们制作另一个包含我们的答案的变量，叫做 safeInt，它包含 maxi 变量的舍入值。这是给定值的安全整数。下面是上面使用的 JavaScript 函数的所有语法:

**语法:**

```
const input = prompt('Please enter umsafe integer:');
var mini = Math.min(input,Number.MAX_SAFE_INTEGER);
var maxi = Math.max(mini,Number.MIN_SAFE_INTEGER);
const safeInt = Math.round(maxi);
```

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <style>
        .gfg1{
            font-size: 30px;
            color: green;
        }
        #gfg2{
            font-size: 30px;
            color: green;    
        }
        div{
            margin-left: 30%;
        }
        button{
            font-size: 20px;
        }
    </style>
</head>
<body>
    <div>
        <p class="gfg1">GeeksforGeeks</p>

        <button onclick="fun()">click me</button>
        <p id="gfg2"></p>

    </div>
    <script>
        function fun(){
            const input = prompt('Please enter umsafe integer:');
            var mini = Math.min(input,Number.MAX_SAFE_INTEGER);
            var maxi = Math.max(mini,Number.MIN_SAFE_INTEGER);
            const safeInt = Math.round(maxi);
            document.getElementById("gfg2").innerHTML = input + " => " + safeInt;
        }
    </script>
</body>
</html>
```

**输出:**

![](img/939fe67a252960649018108cf687fd54.png)