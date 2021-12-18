# JavaScript |注释

> 原文:[https://www.geeksforgeeks.org/javascript-comments/](https://www.geeksforgeeks.org/javascript-comments/)

注释用于阻止语句的执行。编译器执行代码时，注释被忽略。注释是用户友好的，因为用户可以使用注释获得代码的解释。

**语法:**

```
// For single line comment
```

```
/* For block of lines comment
...
...
*/
```

**返回值:**代码执行过程中，注释被忽略。

**示例 1:** 本示例使用//说明单行注释。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript Comments
    </title>

    <script>

        // Function to add two numbers
        function add() {

            // Declare three variables
            var x, y, z;

            // Input a number and store it into variable x
            x = Number( document.getElementById("num1").value );

            // Input a number and store it into variable x
            y = Number( document.getElementById("num2").value );

            // Sum of two numbers
            z= x +y;

            // Return the sum
            document.getElementById("sum").value = z;
        }
    </script>
</head>

<body>
    Enter the First number: <input id="num1"><br><br>
    Enter the Second number: <input id="num2"><br><br>

    <button onclick="add()">
        Sum
    </button>

    <input id="sum">
</body>

</html>                    
```