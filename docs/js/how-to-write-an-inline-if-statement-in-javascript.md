# 如何用 JavaScript 编写内联 IF 语句？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中编写内联 if 语句/](https://www.geeksforgeeks.org/how-to-write-an-inline-if-statement-in-javascript/)

我们可以使用下面描述的方法用 javascript 编写一个内联 **IF** 语句。
**方法 1:** 在这个方法中，我们只使用下面给出的语句编写一个 inline**IF**note else 语句。

**语法:**

```
(a < b) && (your code here)

Above statement is equivalent to
if(a < b){
   // Your code here
}

```

**示例:**以下是上述方法的实现:

```
<script>
    // Javascript script 
    // to write an inline IF
    // statement

    // Function using inline 'if'
    // statement to print maximum
    // number
    function max(n, m){

        // Inline 'if' statement only
        // If n > m then this will execute
        (n > m) && document.write(n + "<br>");
        // Above statement is equivalent to
        // if(n > m){
        //    document.write(n + "<br>");
        // }

        // Inline 'if' statement only
        // If m > n then this will execute
        (m > n) && document.write(m + "<br>");
        // Above statement is equivalent to
        // if(m > n){
        //    document.write(m + "<br>");
        // }
    }

    //Driver code
    var a = -10;
    var b = 5;

    // Call function
    max(a, b);

    // Update value
    a = 50;
    b = 20;

    // Call function
    max(a, b);
</script>
```

**输出:**

```
5
50

```

**方法二:**在这个方法中，我们将使用三元运算符来编写内联 **if** 语句。

**语法:**

```
result = condition ? value1 : value2;

```

如果**条件**为真，则**值 1** 将被分配给**结果**变量，如果错误，则**值 2** 将被分配。

**示例:**以下是上述方法的实现:

```
<script>
    // Javascript script 
    // to write an inline IF
    // statement

    // Function using inline 'if'
    // statement to return maximum
    // number
    function max(n, m){

        // Inline 'if' statement
        // using ternary operator
        var x = (n > m) ? n : m;
        // Above statement is equivalent to
        // if(n > m){
        //    x = n;
        // }
        // else {
        //    x = m;     
        // }

        return x;
    }

    //Driver code
    var a = -10;
    var b = 5;
    var res;

    // Call function
    res = max(a, b);
    // Print result
    document.write(res + "<br>");

    // Update value
    a = 50;
    b = 20;

    // Call function
    res = max(a, b);
    // Print result
    document.write(res + "<br>");
</script>                    
```

**输出:**

```
5
50

```