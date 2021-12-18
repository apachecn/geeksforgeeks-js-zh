# 如何在 JavaScript 中将字符串转换成浮点数？

> 原文:[https://www . geesforgeks . org/如何将字符串转换为 javascript 中的浮点数/](https://www.geeksforgeeks.org/how-to-convert-string-into-float-in-javascript/)

我们可以使用下面描述的一些方法将字符串转换成 JavaScript 中的浮点数:

*   通过使用 JavaScript 的[类型转换](https://www.geeksforgeeks.org/javascript-type-conversion/)
*   通过使用 [parseFloat()](https://www.geeksforgeeks.org/javascript-parsefloat-with-examples/) 方法

**方法 1:** 在此方法中，我们将使用 JavaScript 的[类型转换](https://www.geeksforgeeks.org/javascript-type-conversion/)功能，该功能将字符串值转换为浮点数。

**示例:**下面的程序演示了上述方法

```
<script> 
    // Javascript script  
    // to convert string
    // to float value 

    // Function to convert 
    // string to float value
    function convert_to_float(a) {

        // Type conversion
        // of string to float
        var floatValue = +(a);

        // Return float value
        return floatValue; 
    } 

//Driver code 
var n = "55.225";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");

var n = "-33.565";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");
</script> 
```

**输出:**

```
Converted value = 55.225
Type of 55.225 = number
Converted value = -33.565
Type of -33.565 = number

```

**方法 2:** 在这个方法中，我们将使用 [parseFloat()](https://www.geeksforgeeks.org/javascript-parsefloat-with-examples/) 方法，这是 JavaScript 中的一个内置函数，用于接受字符串并将其转换为浮点数。如果字符串不包含数字值，或者如果字符串的第一个字符不是数字，则返回 **NaN** ，即不是数字。

**示例:**下面的程序演示了上述方法

```
<script> 
    // Javascript script  
    // to convert string
    // to float value 

    // Function to convert 
    // string to float value
    function convert_to_float(a) {

        // Using parseFloat() method
        var floatValue = parseFloat(a);

        // Return float value
        return floatValue; 
    } 

//Driver code 
var n = "245.165";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");

var n = "-915.55";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");
</script> 
```

**输出:**

```
Converted value = 245.165
Type of 245.165 = number
Converted value = -915.55
Type of -915.55 = number

```

**特殊情况:**在**法语**中，浮点数是用**逗号(，**代替**点(。)**作为分离器。
**示例:**

```
The value 245.67 in French is written as 245, 67

```

要在 JavaScript 中将法语字符串转换为浮点数，我们将首先使用 [replace()](https://www.geeksforgeeks.org/javascript-string-replace/) 方法将每一个**()**替换为**(。)**然后遵循任何上述方法。

**示例:**下面的程序演示了上述方法

```
<script> 
    // Javascript script  
    // to convert string
    // to float value 

    // Function to convert 
    // string to float value
    function convert_to_float(a) {

        // Using parseFloat() method
        // and using replace() method
        // to replace ', ' with '.'
        var floatValue = parseFloat(a.replace(/, /, '.'));

        // Return float value
        return floatValue; 
    } 

//Driver code 
var n = "245, 165";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");

var n = "-915, 55";

// Call function 
n = convert_to_float(n); 

// Print result 
document.write("Converted value = " + 
        n + "</br> Type of " + n + " = " 
        +typeof n + "<br>");
</script> 
```

**输出:**

```
Converted value = 245.165
Type of 245.165 = number
Converted value = -915.55
Type of -915.55 = number

```