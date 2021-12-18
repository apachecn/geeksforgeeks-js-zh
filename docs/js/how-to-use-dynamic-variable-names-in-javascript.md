# 如何在 JavaScript 中使用动态变量名？

> 原文:[https://www . geesforgeks . org/如何使用动态变量名 in-javascript/](https://www.geeksforgeeks.org/how-to-use-dynamic-variable-names-in-javascript/)

在编程中，**动态变量名**在脚本中没有硬编码的具体名称。它们是用其他来源的字符串值动态命名的。动态变量很少在 JavaScript 中使用。但在某些情况下，它们是有用的。与 PHP 不同，JavaScript 中没有动态变量名的特殊实现。但是使用一些其他的方法也可以获得类似的结果。在 JavaScript 中，动态变量名可以通过使用下面给出的 2 种方法/途径来实现。

*   **eval():** The eval() function evaluates JavaScript code represented as a string in the parameter. A string is passed as a parameter to eval(). If the string represents an expression, eval() evaluates the expression. Inside eval(), we pass a string in which variable **valuei** is declared and assigned a value of **i** for each iteration. The eval() function executes this and creates the variable with the assigned values. The code is given below implements the creation of dynamic variable names using eval().

    **示例:**

    ```
    <script>
        var k = 'value';
        var i = 0;
        for(i = 1; i < 5; i++) {
            eval('var ' + k + i + '= ' + i + ';');
        }
        console.log("value1=" + value1);
        console.log("value2=" + value2);
        console.log("value3=" + value3);
        console.log("value4=" + value4);
    </script>
    ```

    **输出:**

    ```
    value1=1
    value2=2
    value3=3
    value4=4
    ```

*   **Window object:** JavaScript always has a global object defined. When the program creates global variables they’re created as members of the global object. The window object is the global object in the browser. Any global variables or functions can be accessed with the window object. After defining a global variable we can access its value from the window object. The code given below implements dynamic variable names using the window object. So, the code basically creates a global variable with dynamic name **“valuei”** for each iteration of i and assigns a value of **i** to it. Later these variables can be accessed in the script anywhere as they become global variables.

    **示例:**

    ```
    <script>
        var i;
        for(i = 1; i < 5; i++) {
            window['value'+i] = + i;
        }

        console.log("value1=" + value1);
        console.log("value2=" + value2); 
        console.log("value3=" + value3); 
        console.log("value4=" + value4);
    </script>
    ```

    **输出:**

    ```
    value1=1
    value2=2
    value3=3
    value4=4
    ```

    JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。