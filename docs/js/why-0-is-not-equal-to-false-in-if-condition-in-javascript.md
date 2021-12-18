# 为什么 JavaScript 中 if 条件中的“0”不等于 false？

> 原文:[https://www . geesforgeks . org/why-0-不等于-false-in-if-condition-in-JavaScript/](https://www.geeksforgeeks.org/why-0-is-not-equal-to-false-in-if-condition-in-javascript/)

这种行为背后的原因是 **JavaScript 将非空字符串视为真**。首先，**“0”**通过自动类型转换转换为其**布尔**值，即**真**。因此， **if** 语句执行。

**例:**此例说明了**为什么在 if()条件**中“0”不等于假。

```
<script>

    // JavaScript script to demonstrate 
    // why “0” is not equal to false in
    // ‘if’ condition

    function GFG() {

        // Print type of "0"
        document.write(typeof "0" + "</br>");

        // Print boolean value of "0"
        document.write(Boolean("0") + "</br>");

        // Boolean value of "0" is true so
        // 'if' part will execute
        if("0") {
            document.write("if part executed");
        }
        else {
            document.write("else part executed");
        }
    }

    // Driver code
    GFG();

</script>                    
```

**输出:**

```
string
true
if part executed

```