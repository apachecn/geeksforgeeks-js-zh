# 如何在 JavaScript 中重新抛出异常，但保留堆栈？

> 原文:[https://www . geesforgeks . org/how-rethrow-一个 javascript 中的异常-但保留堆栈/](https://www.geeksforgeeks.org/how-to-rethrow-an-exception-in-javascript-but-preserve-the-stack/)

每当抛出异常时，堆栈跟踪都会传递部分数据。堆栈跟踪是程序中使用的所有方法的集合。它从引发异常的方法开始，到捕获异常的方法结束。如果重新引发异常，堆栈跟踪将在当前方法处重新启动。因此，引发异常的方法和当前方法之间的方法调用列表会丢失。避免这种情况的一种方法是捕获错误并将其存储在本地，然后重新抛出错误。但是，在 JavaScript 中，没有 rethrow()函数。于是我们抛出了最初发生的错误。要理解上述上下文，请参考以下示例。

**例 1:** 在一次班级测试中，拉德哈应该回答老师提出的问题。老师给了拉德哈一个数字，并问她给定的数字是否是有效的日数，如果是，则指定相应的日。如果给定的日数无效，拉德哈应该回答“无效日数”。如果我们运行代码，嵌入的页面将显示堆栈跟踪。它将显示错误起源于第()天，然后在第()个月被重新抛出，最后在第()年被捕获。由于 8 超出界限，因此输出显示为无效日期。

```
Input: 8 
Output:Error originated in day() and was thrown
 Invalid day
 Error was caught and rethrown in month()
 Invalid day
 Error was finally caught in year()
 Invalid day
```

*   **程序:**

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <script>
            year();

            // For the year //
            function year() {
                try {
                    month();

                } catch (e) {
                    console.log(
    'Error was finally caught in year():', e.message);
                    alert(e.stack);
                }
            }

            // Fo the month //
            function month() {
                try {
                    day();
                } catch (e) {
                    console.log(
    'Error was then caught and rethrown in month():', e.message);
                    throw (e);
                }
            }

            function day() {
                var d = 8;
                var days = [
                  'Mon', 'Tue', 'Wed', 
                  'Thurs', 'Fri', 'Sat', 'Sun'];
                try {
                    d = d - 1;
                    if (days[d] != undefined)
                        console.log("valid day:", days[d]);
                    else

                        // Message is "Invalid day"
                        throw new Error("Invalid day"); 
                } catch (e) {
                    console.log(
    "Error originated in day() and was thrown:", e.message)
                    throw (e);

                }
            }
        </script>
    </head>

    <body>
        <h1>Welcome To Geeksforgeeks</h1>
    </body>

    </html>                        
    ```

*   **输出:**

    ```
    Error originated in day() and was thrown:
     Invalid day
     Error was then caught and rethrown in month():
     Invalid day
     Error was finally caught in year():
     Invalid day
    ```

**例 2:** 数字 5 是有效的日数，因此不会抛出错误。因此，我们得到的输出是有效的一天。

```
Input: 5
Output:
valid day:
Fri
```

*   **程序:**

    ```
    <!DOCTYPE html>
    <html>

    <head>
        <script>
            year();

            function year() {
                try {
                    month();

                } catch (e) {
                    console.log(
    'Error was finally caught in year()', e.message);
                    alert(e.stack);
                }
            }

            function month() {
                try {
                    day();
                } catch (e) {
                    console.log(
    'Error was caught and rethrown in month()', e.message);
                    throw (e);
                }
            }

            function day() {
                var d = 5;

                var days = [
                  'Mon', 'Tue', 'Wed', 
                  'Thurs', 'Fri', 'Sat', 'Sun'];
                try {
                    d = d - 1;
                    if (days[d] != undefined)
                        console.log("valid day:", days[d]);
                    else
                        throw new Error("Invalid day");
                } catch (e) {
                    console.log(
    "Error originated in day() and was thrown:", e.message);
                    throw (e);

                }
            }
        </script>
    </head>

    <body>
        <h1>Welcome To Geeksforgeeks</h1>
    </body>

    </html>
    ```

*   **输出:**

    ```
    valid day:
     Fri
    ```