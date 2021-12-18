# 如何用 JavaScript 检查一个变量是函数类型？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 检查变量是否属于函数类型/](https://www.geeksforgeeks.org/how-to-check-a-variable-is-of-function-type-using-javascript/)

JavaScript 中的函数是用于执行特定任务的一组语句。函数可以是命名函数，也可以是匿名函数。函数内部的一组语句在函数被调用时执行。函数可以赋给变量，也可以传递给方法。

```
var gfg = function(){/* A set of statements */};
```

这里，一个匿名函数被分配给名为“gfg”的变量。有各种方法可以检查变量是否属于函数类型。其中一些将在下面讨论:

1.  **Using instanceof operator:** The **instanceof operator** checks the type of an object at run time. It return a corresponding boolean value, i.e, either **true** or **false** to indicate if the object is of a particular type or not.

    **示例:**本示例使用运算符的**实例来检查变量是否属于函数类型。**

    ```
    <script>

    // Declare a variable and initialize it
    // with anonymous function
    var gfg = function(){/* A set of statements */};

    // Function to check a variable is of
    // function type or not
    function testing(x) {

        if(x instanceof Function) {
            document.write("Variable is of function type");
        }
        else {
            document.write("Variable is not of function type");
        }
    }

    // Function call
    testing(gfg);

    </script>                      
    ```

    **输出:**

    ```
    Variable is of function type
    ```

2.  **Using Strict Equal (===) operator:** In JavaScript, ‘===’ Operator is used to check whether two entities are of equal values as well as of equal type provides a boolean result. In this example, we use the **‘===’** operator. This operator, called the Strict Equal operator, checks if the operands are of the same type.

    **示例:**本示例使用 **===** 运算符检查变量是否属于函数类型。

    ```
    <script>

    // Declare a variable and initialize it
    // with anonymous function
    var gfg = function(){/* A set of statements */};

    // Function to check a variable is of
    // function type or not
    function testing(x)
    {   
        if (typeof x === "function") {
            document.write("Variable is of function type");
        }
        else {
            document.write("Variable is not of function type");
        }
    }

    // Function call
    testing(gfg);

    </script>                       
    ```

    **输出:**

    ```
    Variable is of function type
    ```

3.  **Using object.prototype.toString:** This method uses **object.prototype.toString**. Every object has a toString() method, which is called implicitly when a value of String type is expected. If the toString() method is not overridden, by default it returns ‘[object *type*]’ where ‘type’ is the object type.

    **示例:**本示例使用**object . prototype . tostring**运算符检查变量是否属于函数类型。

    ```
    <script>

    // Declare a variable and initialize it
    // with anonymous function
    var gfg = function(){/* A set of statements */};

    // Function to check a variable is of
    // function type or not
    function testing(x)
    {   
        if (Object.prototype.toString.call(x) == '[object Function]')
        {
            document.write("Variable is of function type");

        }
        else {
            document.write("Variable is not of function type");
        }
    }

    // Function call
    testing(gfg);

    </script>     
    ```

    **输出:**

    ```
    Variable is of function type
    ```