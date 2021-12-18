# JavaScript 面试问答|第 2 集

> 原文:[https://www . geesforgeks . org/JavaScript-面试-问答-set-2/](https://www.geeksforgeeks.org/javascript-interview-questions-and-answers-set-2/)

![](img/785984b25214a9e5001c3949ea64c0c1.png)

我们已经在 [JavaScript 面试问答| Set-1](https://www.geeksforgeeks.org/javascript-interview-questions-and-answers/) 中讨论了一些问题。以下是一些更相关的问题:

2.  **[What are all the looping structures in JavaScript ?](https://www.geeksforgeeks.org/loops-in-javascript/)**
    *   **while 循环:**while 循环是一种控制流语句，允许基于给定的布尔条件重复执行代码。while 循环可以看作是一个重复的 if 语句。
    *   **for loop:**for loop 提供了一种编写循环结构的简洁方式。与 while 循环不同，for 语句在一行中消耗初始化、条件和增量/减量，从而提供一个更短、更易于调试的循环结构。
    *   **do while:**do-while 循环类似于 while 循环，唯一的区别是它在执行语句后检查条件，因此是 Exit Control Loop 的一个示例。
3.  **元素的样式/类如何改变？**
    要更改元素的样式/类别，有两种可能的方法。

*   ```
    document.getElementById("myText").style.fontSize = "16px;
    ```

*   ```
    document.getElementById("myText").className = "class";
    ```

*   **Explain how to read and write a file using JavaScript ?**
    *   **[读取文件()](https://www.geeksforgeeks.org/javascript-program-to-read-text-file/)** 功能用于读取操作。

        ```
        readFile( Path, Options, Callback)
        ```

    *   **[写文件()](https://www.geeksforgeeks.org/javascript-program-to-write-data-in-a-text-file/)** 功能用于写操作。

        ```
        writeFile( Path, Data, Callback)

        ```

        *   **What is called Variable typing in JavaScript ?**
    The **variable typing** is the type of variable used to store a number and using that same variable to assign a “string”.

    ```
    Geeks = 42;
    Geeks = "GeeksforGeeks";
    ```

    *   **[How to convert the string of any base to integer in JavaScript ?](https://www.geeksforgeeks.org/convert-a-string-to-an-integer-in-javascript/)**
    In JavaScript, parseInt() function is used to convert the string to an integer. This function returns an integer of base which is specified in second argument of parseInt() function. The parseInt() function returns Nan (not a number) when the string doesn’t contain number.*   **[Explain how to detect the operating system on the client machine ?](https://www.geeksforgeeks.org/how-to-detect-operating-system-on-the-client-machine-using-javascript/)**
    To detect the operating system on the client machine, one can simply use navigator.appVersion or navigator.userAgent property. The Navigator appVersion property is a read-only property and it returns the string that represents the version information of the browser.*   **[What are the types of Pop up boxes available in JavaScript ?](https://www.geeksforgeeks.org/what-are-the-types-of-popup-box-available-in-javascript/)**
    There are three types of pop boxes available in JavaScript.
    *   警报
    *   确认
    *   提示

    *   **[What is the difference between an alert box and a confirmation box ?](https://www.geeksforgeeks.org/what-are-the-types-of-popup-box-available-in-javascript/)**
    An alert box will display only one button which is the OK button. It is used to inform the user about the agreement has to agree. But a Confirmation box displays two buttons OK and cancel, where the user can decide to agree or not.*   **What is the disadvantage of using innerHTML in JavaScript ?**
    There are lots of disadvantages of using the innerHTML in JavaScript like the content will replace everywhere. If you use += like “innerHTML = innerHTML + ‘html'” still the old content is replaced by HTML. It preserves event handlers attached to any DOM elements.*   **[What is the use of void(0) ?](https://www.geeksforgeeks.org/what-does-javascriptvoid0-mean/)**
    The void(0) is used to call another method without refreshing the page during the calling time parameter “zero” will be passed.*   **What are JavaScript Cookies ?**
    Cookies are small files that are stored on a user’s computer. They are used to hold a modest amount of data specific to a particular client and website and can be accessed either by the web server or by the client computer. When cookies were invented, they were basically little documents containing information about you and your preferences. For instance, when you select your language in which you want to view your website, the website would save the information in a document called a cookie on your computer, and the next time when you visit the website, it would be able to read a cookie saved earlier.*   **How to create a cookie using JavaScript ?**
    To create a cookie by using JavaScript you just need to assign a string value to the document.cookie object.

    ```
    document.cookie = "key1 = value1; key2 = value2; expires = date";
    ```

    *   **How to read a cookie using JavaScript ?**
    The value of the **document.cookie** is used to create a cookie. Whenever you want to access the cookie you can use the string. The **document.cookie** string keep a list of **name = value** pairs separated by semicolons, where **name** is the *name of a cookie* and the **value** is its *string value*.*   **How to delete a cookie using JavaScript ?**
    Deleting cookie is much easier than creating or reading a cookie, you just need to set the expires = “past time” and make sure one thing defines the right cookie path unless few will not allow you to delete the cookie.*   **What are escape characters and escape() function ?**
    *   **转义字符:**当您想要使用单引号和双引号、撇号和&符号等特殊字符时，此字符是必需的。所有的特殊字符在 JavaScript 中都起着重要的作用，要忽略或打印该特殊字符，可以使用转义字符**反斜杠“\”**。它通常会忽略并表现得像一个正常的角色。

        ```
        // Need escape character
        document.write("GeeksforGeeks: A Computer Science Portal "for Geeks" ")
        document.write("GeeksforGeeks: A Computer Science Portal \"for Geeks\" ")
        ```

    *   **[escape()函数:](https://www.geeksforgeeks.org/javascript-escape/)**escape()函数以一个字符串为参数，对其进行编码，使其可以传输到任何支持 ASCII 字符的网络中的任何一台计算机上。*   **Whether JavaScript has a concept level scope ?**
    JavaScript is not concept level scope, its declared the variable inside any function has scope inside the function.*   **How generic objects can be created in JavaScript ?**
    To create a generic object in JavaScript use

    ```
    var I = new object();
    ```

    *   **[Which keywords are used to handle exceptions ?](https://www.geeksforgeeks.org/javascript-errors-throw-and-try-to-catch/)**
    When executing JavaScript code, errors will almost definitely occur. These errors can occur due to the fault from the programmer’s side due to the wrong input or even if there is a problem with the logic of the program. But all errors can be solved by using the below commands.
    *   **try** 语句允许您测试一段代码来检查错误。
    *   如果存在任何错误，可以使用 **catch** 语句来处理错误。
    *   **throw** 语句让你自己犯错误。*   **[What is the use of the blur function ?](https://www.geeksforgeeks.org/jquery-blur-with-examples/)**
    It is used to remove focus from the selected element. This method starts the blur event or it can be attached a function to run when a blur event occurs.*   **[JavaScript 中的 unshift 方法是什么？](https://www.geeksforgeeks.org/javascript-array-prototype-unshift-function/)**
    用于在数组前插入元素。就像一个 [**推**](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/) 的方法，在数组的开头插入元素。