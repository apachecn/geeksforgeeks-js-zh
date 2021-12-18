# 抛出异常时如何获取 JavaScript 堆栈跟踪？

> 原文:[https://www . geesforgeks . org/如何获取 JavaScript-堆栈-异常时跟踪/](https://www.geeksforgeeks.org/how-to-get-javascript-stack-trace-when-throw-an-exception/)

堆栈跟踪是一种稳定的方法，用于识别调用程序的函数时进入程序的错误。它帮助程序员检查特定的错误/异常来自哪里，以及其背后的原因是什么。根据收集跟踪数据的时间，这些跟踪的文件大小可能会很大。当抛出错误/异常时，我们必须找到一种方法来获取 JavaScript 堆栈跟踪。

堆栈跟踪是程序执行过程中特定时间点的活动堆栈帧的报告。当程序运行时，内存通常在堆栈和堆中动态分配。与堆相比，堆栈更活跃，因为它通常是一个连续的内存区域，为每个正在执行的函数分配本地上下文。堆栈也指编程构造，所以这个堆栈被称为程序的运行时堆栈。一旦堆栈上分配了一块内存。它不容易移除，因为在它之前可能分配了其他内存块。每次在程序中调用函数时，都会在运行时堆栈的顶部分配一块内存，称为激活记录。程序员通常在交互和调试过程中使用堆栈跟踪。最终用户可能会看到堆栈跟踪显示为错误消息的一部分，用户可以向程序员报告。

**栈**是一种数据结构类型，其中数据可以以**后进先出(LIFO)** 的形式存储。这意味着堆栈是一种存储类型，当一组数据进入堆栈时，它会以最后一个数据先移除，最后一个数据最后移除的方式逐个存储。堆栈跟踪可以理解从堆栈中删除任何数据存储组的方式。
在抛出异常时，我们可以通过以下方法获取 JavaScript 的堆栈跟踪。

*   **控制台. trace***   **错误对象***   **caller Object**

    **使用 console . trace:**console 对象还有一个叫 **console.trace()方法**的方法，给你控制台上的跟踪。每次调用它时，都会为函数生成堆栈跟踪。借助这个例子，我们可以理解这一点。

    *   **程序:**

        ```
        // Sum function
        function sum(a, b) {
            console.trace('sum called with ', a, 'and', b);
            return a+b;
        }

        // Calculation function 
        function calc() {
            return sum(8, 11) + sum(9, 14);
        }

        // Start function
        function start() {
            var a = sum(2, 3);
            var b = calc();
        }

        // Calling start function 
        start();
        ```

    *   **输出:**

        ```
        /usr/bin/node stacktrace.js
        Trace: add called with  2 and 3
            at sum (/home/dev/Documents/stacktrace.js:2:13)
            at start (/home/dev/Documents/stacktrace.js:11:13)
            at Object. (/home/dev/Documents/stacktrace.js:16:1)
            at Module._compile (internal/modules/cjs/loader.js:959:30)
            at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
            at Module.load (internal/modules/cjs/loader.js:815:32)
            at Function.Module._load (internal/modules/cjs/loader.js:727:14)
            at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
            at internal/main/run_main_module.js:17:11
        Trace: add called with  8 and 11
            at sum (/home/dev/Documents/stacktrace.js:2:13)
            at calc (/home/dev/Documents/stacktrace.js:7:12)
            at start (/home/dev/Documents/stacktrace.js:12:13)
            at Object. (/home/dev/Documents/stacktrace.js:16:1)
            at Module._compile (internal/modules/cjs/loader.js:959:30)
            at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
            at Module.load (internal/modules/cjs/loader.js:815:32)
            at Function.Module._load (internal/modules/cjs/loader.js:727:14)
            at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
            at internal/main/run_main_module.js:17:11
        Trace: add called with  9 and 14
            at sum (/home/dev/Documents/stacktrace.js:2:13)
            at calc (/home/dev/Documents/stacktrace.js:7:25)
            at start (/home/dev/Documents/stacktrace.js:12:13)
            at Object. (/home/dev/Documents/stacktrace.js:16:1)
            at Module._compile (internal/modules/cjs/loader.js:959:30)
            at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
            at Module.load (internal/modules/cjs/loader.js:815:32)
            at Function.Module._load (internal/modules/cjs/loader.js:727:14)
            at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
            at internal/main/run_main_module.js:17:11

        ```

    **使用错误对象:**我们可以创建一个**错误对象**并返回**堆栈**属性。**错误对象**的非标准**堆栈**属性为您提供了从哪一行和哪一个文件调用特定函数时的堆栈跟踪，以及使用了哪些参数。堆栈字符串从最近的调用前进到较早的调用。

    *   **程序:**

    ```
    // Sum function
    function sum(a, b) {
        console.log(new Error().stack);
        return a+b;
    }

    // Calculation function 
    function calc() {
        return sum(8, 11) + sum(9, 14);
    }

    // Start function 
    function start() {
        var a = sum(2, 3);
        var b = calc();
    }

    // Calling start function 
    start();
    ```

    *   **Output:**

    ```
    /usr/bin/node trace.js
    Error
        at sum (/home/dev/Documents/trace.js:2:17)
        at start (/home/dev/Documents/trace.js:11:13)
        at Object. (/home/dev/Documents/trace.js:16:1)
        at Module._compile (internal/modules/cjs/loader.js:959:30)
        at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
        at Module.load (internal/modules/cjs/loader.js:815:32)
        at Function.Module._load (internal/modules/cjs/loader.js:727:14)
        at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
        at internal/main/run_main_module.js:17:11
    Error
        at sum (/home/dev/Documents/trace.js:2:17)
        at calc (/home/dev/Documents/trace.js:7:12)
        at start (/home/dev/Documents/trace.js:12:13)
        at Object. (/home/dev/Documents/trace.js:16:1)
        at Module._compile (internal/modules/cjs/loader.js:959:30)
        at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
        at Module.load (internal/modules/cjs/loader.js:815:32)
        at Function.Module._load (internal/modules/cjs/loader.js:727:14)
        at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
        at internal/main/run_main_module.js:17:11
    Error
        at sum (/home/dev/Documents/trace.js:2:17)
        at calc (/home/dev/Documents/trace.js:7:25)
        at start (/home/dev/Documents/trace.js:12:13)
        at Object. (/home/dev/Documents/trace.js:16:1)
        at Module._compile (internal/modules/cjs/loader.js:959:30)
        at Object.Module._extensions..js (internal/modules/cjs/loader.js:995:10)
        at Module.load (internal/modules/cjs/loader.js:815:32)
        at Function.Module._load (internal/modules/cjs/loader.js:727:14)
        at Function.Module.runMain (internal/modules/cjs/loader.js:1047:10)
        at internal/main/run_main_module.js:17:11

    ```

    **使用调用者对象:**我们实现了一个名为 **stacktrace** 的函数，该函数将返回一个字符串，该字符串表示调用历史到调用 **stacktrace()** 的点。在内部，它使用另一个名为 **st2** 的函数，该函数将被递归调用，遍历调用树，直到到达 JavaScript 脚本的主体。在 stacktrace 声明的末尾，我们用**参数调用 **st2** 。arguments 是一个属于当前函数调用的特殊对象，它包含了大量关于当前调用的信息。然后递归调用 **st2** 函数，并返回到目前为止的 stacktrace 字符串。**

    *   **程序:**

        ```
        // Sum function
        function sum(a,b) {

            // Calling stacktrace function
            console.log(stacktrace()); 
            return a+b;
        }

        // Calculation function 
        function calc() {
            return sum(8, 11) + sum(9, 14);
        }

        // Start function 
        function start() {
            var a = sum(2, 3);
            var b = calc();
        }

        // Calling start function 
        start();

        // Stacktrace function 
        function stacktrace() {
          function st2(f) {
            var args = [];
            if (f) {
                for (var i = 0; i < f.arguments.length; i++) {
                    args.push(f.arguments[i]);
                }
                var function_name = f.toString().
                split('(')[0].substring(9);
                return st2(f.caller) + function_name + 
                '(' + args.join(', ') + ')' + "\n";
            } else {
                return "";
            }
          }
          return st2(arguments.callee.caller);
        }
        ```

    *   **输出:**

        ```
        /usr/bin/node stackt.js
        ([object Object], function require(path) {
              return mod.require(path);
            }, [object Object], /home/dev/Documents/stackt.js, /home/dev/Documents)
        start()
        sum(2, 3)
        ([object Object], function require(path) {
              return mod.require(path);
            }, [object Object], /home/dev/Documents/stackt.js, /home/dev/Documents)
        start()
        calc()
        sum(8, 11)
        ([object Object], function require(path) {
              return mod.require(path);
            }, [object Object], /home/dev/Documents/stackt.js, /home/dev/Documents)
        start()
        calc()
        sum(9, 14)

        ```