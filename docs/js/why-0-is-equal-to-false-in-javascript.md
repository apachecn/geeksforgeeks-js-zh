# JavaScript 中为什么“0”等于假？

> 原文:[https://www . geesforgeks . org/why-0-等于-false-in-javascript/](https://www.geeksforgeeks.org/why-0-is-equal-to-false-in-javascript/)

在 JavaScript 中**“0”**等于**假**因为**“0”**是类型**字符串**但是当它测试相等时，JavaScript 的自动[类型转换](https://www.geeksforgeeks.org/javascript-type-conversion/)生效并将**“0”**转换为它的**数字**值，也就是 **0** ，我们知道 **0** 代表**假所以，**“0”**等于**假**。**

**例:**此例说明了**为什么“0”等于假**。

```
<script>

    // JavaScript code to demonstrate 
    // why “0” is equal to false

    function GFG() {

        // Print type of "0"
        document.write(typeof "0" + "</br>");

        // Test whether "0" equals to false
        // or not. If "0" is equal to false
        // then "0" == false i.e.
        // false == false which return true
        var result = ("0" == false);

        // Print result
        document.write(result + "</br>");

        // Convert and print "0" to its numeric
        // value
        document.write(Number("0") + "</br>");

        // Convert and print false in numeric value
        document.write(Number(false) + "</br>");

        // So both numeric value are same
        // Therefore condition "0" == false
        // evaluates to true
        document.write("0" == false);
        document.write("</br>");

        // Or this statement
        document.write(Number("0") == Number(false));
    }

    // Driver code
    GFG();

</script>
```

**输出:**

```
string
true
0
0
true
true

```

所以，从上可知**“0”等于假**，这种行为背后的原因也很清楚，但是当**“0”**在**测试如果条件**时，则评估为**真**。