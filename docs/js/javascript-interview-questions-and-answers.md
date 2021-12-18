# JavaScript 面试问答

> 原文:[https://www . geesforgeks . org/JavaScript-面试-问答/](https://www.geeksforgeeks.org/javascript-interview-questions-and-answers/)

![](img/785984b25214a9e5001c3949ea64c0c1.png)

1.  **[What are the differences between Java and JavaScript ?](https://www.geeksforgeeks.org/difference-between-java-and-javascript/)**
    JavaScript is a client-side scripting language and Java is object Oriented Programming language, both of them are totally different from each other.
    *   **[JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) :** 它是一种轻量级编程语言(“脚本语言”)，用于开发交互式网页。它可以在 HTML 元素中插入动态文本。JavaScript 也被称为浏览器的语言。
    *   **[Java](https://www.geeksforgeeks.org/java/) :** Java 是最流行、使用最广泛的编程语言之一。它是一种面向对象的编程语言，并且有一个虚拟机平台，允许您创建几乎在每个平台上运行的编译程序。Java 承诺，“只写一次，随处运行”。
2.  **[什么是 JavaScript 数据类型？](https://www.geeksforgeeks.org/variables-datatypes-javascript/)**
    JavaScript 中有三种主要的数据类型。

*   原始的
    *   数字
    *   用线串
    *   布尔代数学体系的
*   不重要的
    *   空
    *   不明确的
*   复合材料
    *   目标
    *   功能
    *   数组

*   **[Which symbol is used for comments in JavaScript ?](https://www.geeksforgeeks.org/javascript-comments/)**
    Comments are used to prevent the execution of statements. Comments are ignored while the compiler executes the code. There are two type of symbols used to represent comment in JavaScript:
    *   **双斜线:**被称为单行注释。

        ```
        // Single line comment
        ```

    *   **带星号的斜线:**被称为多行注释。

        ```
        /* 
        Multi-line comments
        ...
        */
        ```

        *   **What would be the result of 3+2+”7″ ?**
    Here 3 and 2 behave like an integer and “7” behaves like a string. So 3 plus 2 will 5\. Then the output will be 5+”7″ = 57.*   **[What is the use of isNaN function ?](https://www.geeksforgeeks.org/number-isnan-javascript/)**
    The Number.isNan function in JavaScript is used to determines whether the passed value is NaN (Not a Number) and is of the type “Number”. In JavaScript, the value NaN is considered a type of number. It returns true if the argument is not a number else it returns false.*   **Which is faster in JavaScript and ASP script ?**
    The JavaScript is faster compare to ASP Script because JavaScript is a client-side scripting language and does not depend on the server to execute it but the ASP script is a server-side scripting language always dependable on the server.*   **[What is negative infinity ?](https://www.geeksforgeeks.org/what-is-negative-infinity-in-javascript/)**
    The negative infinity in JavaScript is a constant value that is used to represent the lowest available value. It means that no other number is lesser than this value. It can be generated using a self-made function or by an arithmetic operation. JavaScript shows the NEGATIVE_INFINITY value as -Infinity.*   **Is it possible to break JavaScript Code into several lines ?**
    Yes, it is possible to break the JavaScript code into several lines in string statement. It can be break by using the **backslash ‘\’**. For example:

    ```
    document.write("A Online Computer Science Portal\ for Geeks")
    ```

    JavaScript 避免了代码换行，这是不可取的。

    ```
    var gfg= 10, GFG = 5,
    Geeks =
    gfg + GFG;
    ```

    *   **Which company developed JavaScript ?**
    Netscape developed the JavaScript and created by Brenden Eich in the year of 1995.*   **[What are undeclared and undefined variables ?](https://www.geeksforgeeks.org/what-are-undeclared-and-undefined-variables-in-javascript/)**
    *   **未定义:**当一个变量已经被声明，但没有被赋值时，就会出现这种情况。Undefined 不是关键字。
    *   **未声明:**当我们尝试使用 var 或 const 关键字访问任何未初始化或未提前声明的变量时，就会出现这种情况。如果我们使用“typeof”运算符来获取未声明变量的值，我们将面临返回值为“undefined”的运行时错误。未声明变量的范围总是全局的。*   **Write a JavaScript code for adding new elements dynamically ?**

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <title>
            JavaScript code for adding new
            elements dynamically
        </title>
    </head>

    <body>
        <button onclick="create()">
            Click Here!
        </button>

        <script>
            function create() {
                var geeks = document.createElement('geeks');
                geeks.textContent = "Geeksforgeeks";
                geeks.setAttribute('class', 'note');
                document.body.appendChild(geeks);
            }
        </script>
    </body>

    </html>
    ```

    *   **[What are global variables? How are these variable declared and what are the problems associated with them ?](https://www.geeksforgeeks.org/global-and-local-variables-in-javascript/)**
    In contrast, global variables are the variables that are defined outside of functions. These variables have a global scope, so they can be used by any function without passing them to the function as parameters.
    **Example:**

    ```
    <script> 
         var petName = "Rocky"; //Global Variable 
         myFunction(); 

         function myFunction() { 
             document.getElementById("geeks").innerHTML
                          = typeof petName + "- " + 
                          "My pet name is " + petName; 
         } 

         document.getElementById("Geeks").innerHTML
                          = typeof petName + "- " + 
                          "My pet name is " + petName; 
    </script> 
    ```

    很难调试和测试依赖全局变量的代码。

    *   **What do you mean by NULL in JavaScript ?**
    The NULL value represents the no value or no object. It can be called as empty value/object.*   **How to delete property specific value ?**
    The delete keyword is used to delete the whole property and all the values at once like

    ```
    var gfg={Course: "DSA", Duration:30};
    delete gfg.Course;
    ```

    *   **[What is a prompt box ?](https://www.geeksforgeeks.org/javascript-window-prompt-method/)**
    It is used to display a dialog box with an optional message prompting the user to input some text. It is often used if the user wants to input a value before entering a page. It returns a string containing the text entered by the user, or null.*   **[What is ‘this’ keyword in JavaScript ?](https://www.geeksforgeeks.org/this-in-javascript/)**
    Functions in JavaScript are essential objects. Like objects, they can be assigned to variables, passed to other functions and returned from functions. And much like objects, they have their own properties.
    ‘this’ stores the current execution context of the JavaScript program. Thus, when it used inside a function, the value of ‘this’ will change depending on how the function is defined, how it is invoked and the default execution context.*   **[Explain the working of timers in JavaScript? Also elucidate the drawbacks of using the timer, if any ?](https://www.geeksforgeeks.org/javascript-timer/)**
    Timer is used to execute some specific code at specific time or any small amount of code in repetition to do that you need to use the function **setTimout**, **setInterval** and **clearInterval**. If JavaScript code set the timer of 2 minutes and when the times up then the page display an alert message “times up”. The **setTimeout()** method calls a function or evaluates an expression after a specified number of milliseconds.*   **What is the difference between ViewState and SessionState ?**
    *   **视图状态:**特定于会话中的单个页面。
    *   **SessionState:** 是用户特定的，可以访问网页中的所有数据。*   **How can you submit a form using JavaScript ?**
    You can use **document.form[0].submit()** method to submit the form in JavaScript.*   **Does JavaScript support automatic type conversion ?**
    Yes, JavaScript supports automatic type conversion.

    **相关文章:** [常见 JavaScript 面试问题|第一集](https://www.geeksforgeeks.org/commonly-asked-javascript-interview-questions-set-1/)