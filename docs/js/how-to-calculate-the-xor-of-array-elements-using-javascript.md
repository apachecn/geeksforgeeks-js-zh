# 如何用 JavaScript 计算数组元素的 XOR？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 计算数组元素的异或/](https://www.geeksforgeeks.org/how-to-calculate-the-xor-of-array-elements-using-javascript/)

给定一个数组，任务是使用 JavaScript 找到数组元素的异或。有两种方法可以解决这个问题，讨论如下:

**简单方法:**它使用一个简单的方法，通过一个索引号来访问数组元素，并使用循环使用 JavaScript 来找到一个数组的值的 XOR。

**示例:**这个示例使用一个简单的方法，使用 JavaScript 找到 Array 元素的 XOR。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        How to Find the XOR of Values 
        of an Array in JavaScript? 
    </title> 
</head> 

<body style="text-align:center;"> 

    <h1 style = "color:green;" > 
        GeeksForGeeks 
    </h1> 

    <h3> 
        How to Find the XOR of Values 
        of an Array in JavaScript? 
    </h3> 

    <h4> 
        ----Given Array----<br> 
        [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
    </h4> 

    <button onclick="myGeeks()">Click</button> 

    <p id="gfg"></p> 

    <script> 
        function XOR(input)
        { 
            if (toString.call(input) !== "[object Array]") 
            return false; 

            var total = Number(input[0]); 
            for(var i=1;i<input.length;i++) {                 
                if(isNaN(input[i])){ 
                    continue; 
                } 

                total ^= Number(input[i]); 
            } 
            return total; 
        } 
        function myGeeks(item) { 
                document.getElementById("gfg").innerHTML
                    = "----XOR of Array----" + "<br>" 
                    + XOR([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]); 
            }
    </script> 
</body> 

</html>                    
```

**输出:**

*   **之前点击按钮:**
    ![](img/e3efda3b55ba6dab72e63ea8e87c080a.png)
*   **点击按钮后:**
    ![](img/016ef7424273f63464df62d59da69bb1.png)

**使用 [reduce()方法](http://geeksforgeeks.org/javascript-array-reduce-method/):**JavaScript 中的 array reduce()方法用于将数组缩减为单个值，并为数组的每个值(从左到右)执行一个提供的函数，该函数的返回值存储在累加器中。

**语法:**

```
array.reduce( function( total, currentValue, currentIndex, arr ), initialValue )
```

**示例:**本示例使用 array reduce()方法，使用 JavaScript 查找 array 的值的 XOR。

```
<!DOCTYPE html> 
<html> 

<head> 
    <title> 
        How to Find the XOR of Values 
        of an Array in JavaScript? 
    </title> 
</head> 

<body style="text-align:center;"> 

    <h1 style = "color:green;" > 
        GeeksForGeeks 
    </h1> 

    <h3> 
        How to Find the XOR of Values 
        of an Array in JavaScript? 
    </h3> 

    <h4> 
        ----Given Array----<br> 
        [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
    </h4> 

    <button onclick="myGeeks()"> 
        Click Here! 
    </button> 

    <br><br> 

    XOR: <span id="GFG"></span> 

    <script> 
        var arr=[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; 

        function ORofArray(XOR, num) { 
            return XOR ^ num; 
        } 
        function myGeeks(item) { 
            document.getElementById("GFG").innerHTML 
                = arr.reduce(ORofArray); 
        } 
    </script> 
</body> 

</html>                    
```

**输出:**

*   **之前点击按钮:**
    ![](img/e65ec8d3abe58bfd16a030d3f54c9cec.png)
*   **点击按钮后:**
    ![](img/30d9e6bb9161424b5a4acbda8c8d388e.png)