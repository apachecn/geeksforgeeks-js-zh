# 如何在 JavaScript 中终止一个脚本？

> 原文:[https://www . geesforgeks . org/如何终止 javascript 脚本/](https://www.geeksforgeeks.org/how-to-terminate-a-script-in-javascript/)

在本文中，我们将讨论在 JavaScript 中终止脚本的不同方法。

**1。使用 return:** 为了终止脚本的某个部分，可以在该特定范围内包含一个 return 语句。

*   **Terminating the entire Script:**

    ```
    <script>
        var i = 10;

        // Return statement is in 
        // the global scope
        if (i === 10)
            return;

        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
        document.write('This section will not be executed');
        document.write('<br>');

        document.write(arr.filter(
                (elem, index) => { return elem > 2 }));
    </script>
    ```

    **输出:**

*   **无退货声明时:**

    ```
    This section will not be executed
    3, 4, 5, 6, 7, 8, 9
    ```

*   **In the presence of return:**

    不会显示输出，因为程序在遇到时被终止。

**2。终止脚本的一部分:**

```
<script>
    function doSomeThing() {
        var i = 10;
        if (i === 10)
            return;

        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

        document.write(
            'This section will not be executed');
        document.write(arr.filter(
            (elem, index) => { return elem > 2 }));
    }

    let i = doSomeThing();
    if (i === undefined)
        document.write('Terminated');
</script>
```

**输出:**

```
Terminated
```

**解释:**根据条件，可以使用“return”语句终止脚本的某个部分。“return”语句将“undefined”返回到直接父作用域，在那里可以处理终止。这是最佳实践，因为处理终止使将来的调试和代码的可读性更容易。

**3。故意抛出错误:**

```
<script>
    function doSomeThing() {
        var i = 10;
        if (i === 10)
            throw new Error(
                'Program Terminated');

        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

        document.write(
            'this section will not be executed');

        document.write(arr.filter(
            (elem, index) => { return elem > 2 }));
    }

    try {
        doSomeThing();
    }
    catch (err) {
        document.write(err.message);
    }
```

**输出:**

```
Program Terminated

```

**解释:**我们故意抛出一个错误来终止我们想要终止的脚本部分。最佳实践是使用“try catch”块来处理错误。

**4。使用进程。退出节点。JS 应用:**

```
<script>
    function doSomeThing() {
        var i = 10;
        document.write('Terminating ');
        process.exit(0);
        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

        document.write(
            'This section will not be executed');

        document.write(arr.filter(
            (elem, index) => { return elem > 2 }));
    }
    doSomeThing();
</script>
```

**输出:**

```
Terminating:
```

在这种情况下，不会有其他输出，因为我们退出了脚本。这适用于**节点**环境中的所有 JavaScript 应用程序。NodeJS 中还有许多其他方法，例如`process.kill(process.pid)`和`process.abort()`，但是 process.exit()即使不是所有的情况，也足以满足大多数情况。