# JavaScript 三元运算符

> 原文:[https://www.geeksforgeeks.org/javascript-ternary-operator/](https://www.geeksforgeeks.org/javascript-ternary-operator/)

下面是三元运算符的示例。

*   **例:**
    **程序一:**

    ```
    <script>  
        function gfg() {  
         //JavaScript to illustrate 
        //Conditional operator 

        let PMarks = 40 
        let result = (PMarks > 39)? 
            "Pass":"Fail"; 

        document.write(result); 
        }  
        gfg();  
    </script> 
    ```

*   **输出:**

    ```
    Pass
    ```

**“问号”**或**“条件”**运算符在 JavaScript 中是一个有三个操作数的三元运算符。

*   该表达式由三个操作数组成:*条件*、如果*为真则值*以及如果*为假则值。*
*   对**条件**的评估应得出真/假或布尔值。
*   **真**值介于“**之间？**“&”**:**”条件返回真时执行。类似地，**假**值位于**:**之后，如果条件返回假，则执行。

**语法:**

```
condition ? value if true : value if false
```

**condition:**
*   Expression to be evaluated which returns a boolean value.

    **真值:**

*   Value to be executed if condition results in true state.

    **值为假:**

*   条件导致假状态时要执行的值。

**示例:**

```
Input: let result = (10 > 0) ? true : false;
Output: true

Input: let message = (20 > 15) ? "Yes" : "No";
Output: Yes

```

以下程序将更详细地说明**条件**运算符:

**程序 1:**

```
<script>  
    function gfg() {  
     //JavaScript to illustrate 
    //Conditional operator 

    let age = 60 
    let result = (age > 59)? 
        "Senior Citizen":"Not a Senior Citizen"; 

    document.write(result); 
    }  
    gfg();  
</script>                  
```

**输出:**

```
Senior Citizen
```

多个条件运算符的示例。
**节目 2:**

```
<script>  
    function gfg() {  
    //JavaScript to illustrate
    //multiple Conditional operators

    let marks = 95;
    let result = (marks < 40) ? "Unsatisfactory" : 
             (marks < 60) ? "Average" :
             (marks < 80) ? "Good" : "Excellent" ;

    document.write(result);
    }  
    gfg();  
</script> 
```

**输出:**

```
Excellent
```