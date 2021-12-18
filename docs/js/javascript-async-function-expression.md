# JavaScript |异步函数表达式

> 原文:[https://www . geesforgeks . org/JavaScript-async-function-expression/](https://www.geeksforgeeks.org/javascript-async-function-expression/)

异步函数表达式用于在 JavaScript 表达式中定义异步函数。异步函数是使用 async 关键字声明的。
**语法:**

```
async function [function_name]([param1[, param2[, ..., paramN]]]) {
    // Statements
}
```

**参数:**

*   **函数名:**此参数保存函数名。该函数名是函数体的本地名称。如果函数名是匿名的，那么它就变成了匿名函数。
*   **参数名:**是要传递到函数中的参数名。
*   **语句:**包含函数体。

**返回值:**每当发生错误时，它都会返回一个返回值的承诺，否则抛出异常。
**示例 1:** 在此示例中，首先打印“GeeksforGeeks”，间隔 1000 ms 后打印“GFG”。

## java 描述语言

```
<script>
    function cb() {
        return new Promise(function (resolve, reject) {
            setTimeout(function () {
                resolve("GFG")
            }, 1000)

        })
    }
    async function course() {
        console.log("GeeksforGeeks");
        const result = await cb();
        console.log(result);
    }

    course();
</script>
```

**输出:**

```
GeeksforGeeks
GFG
```

**示例 2:** 在这里，制作一个文件 *gfg.txt* ，文件一被读取，它就在控制台中打印“读取文件”。否则，当文件位置错误或由于任何其他原因无法读取文件时，它会打印“错误”。

## java 描述语言

```
<script>
    async function gfg() {
        try {
            let f1 = await fs.promises.readFile("gfg.txt")
            console.log("Read the file")
        }
        catch (err) {
            console.log("error");
        }
    }
    gfg();
</script>
```

**输出:**

*   **当文件读:**

```
Read the file
```

*   **文件未读取时(抛出错误)**

```
error
```

**示例 3:** 这是异步函数并行工作的示例。

## java 描述语言

```
<script>
    function cb() {
        return new Promise(function (resolve, reject) {
            setTimeout(function () {
                resolve("GFG")
            }, 2000)

        })
    }

    function cb1() {
        return new Promise(function (resolve, reject) {
            setTimeout(function () {
                resolve("GFG1")
            }, 1000)

        })
    }

    async function course() {
        console.log("GeeksforGeeks");
        const result1 = await cb1();
        const result = await cb();
        console.log(result1);
        console.log(result);
    }

    course();
</script>
```

**输出:**

```
GeeksforGeeks
GFG1
GFG
```

**支持的浏览器:**

*   谷歌 Chrome 55 及以上
*   边缘 15 及以上
*   Firefox 52 及以上版本
*   Safari 10.1 及以上版本
*   歌剧 42 及以上