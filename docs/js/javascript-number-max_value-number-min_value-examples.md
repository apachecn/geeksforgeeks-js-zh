# JavaScript 编号。最大值&数字。最小值属性

> 原文:[https://www . geesforgeks . org/JavaScript-number-max _ value-number-min _ value-examples/](https://www.geeksforgeeks.org/javascript-number-max_value-number-min_value-examples/)

下面是数字的例子。最大值和数值。最小值属性。

*   **例:**

    ```
    <script> 
    function GFGFun() { 
        document.write(Number.MAX_VALUE+"<br>");
        document.write(Number.MIN_VALUE+"<br>");
    } 
    GFGFun(); 
    </script> 
    ```

*   **输出:**

    ```
    1.7976931348623157e+308
    5e-324

    ```

**数字。最大值**和**号。MIN_VALUE** 用于在 javascript 中表示最大和最小数值。

**语法:**

```
Number.MAX_VALUE 
Number.MIN_VALUE 

```

**返回类型:**
均为数字。最大值和数值。最小值返回一个数值。

*   MAX_VALUE 的值约为 1.79E+308。大于数字的值。最大值被称为**无穷大。**
*   最小值约为 5e-324。小于数字的值。最小值被称为**下溢值。**
*   最大值和最小值都是数字的静态属性。因此，使用 x.MAX_VALUE 或 x.MIN_VALUE 将返回未定义，其中 x 是数字或数字对象。

**例 1:**

```
Input : Number.MAX_VALUE
Output : 1.7976931348623157e+308
```

**例 2:**

```
Input : Number.MIN_VALUE
Output : 5e-324
```

**程序:**

```
<script> 

function GFGFun() { 
    // JavaScript Code to illustrate Number.MAX_VALUE
    // & Number.MIN_VALUE
    document.write(Number.MAX_VALUE+"<br>");
    document.write(Number.MIN_VALUE+"<br>");

    // Undefined Behaviour 
    var res = 1; 
    res = res.MAX_VALUE; 
    document.write(res); 
} 
GFGFun(); 
</script> 
```

**输出:**

```
1.7976931348623157e+308
5e-324
undefined
```