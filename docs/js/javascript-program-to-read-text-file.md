# Javascript |读取文本文件的程序

> 原文:[https://www . geesforgeks . org/JavaScript-程序到读取-文本-文件/](https://www.geeksforgeeks.org/javascript-program-to-read-text-file/)

**先决条件:**如何在 JavaScript 中导入库。从这里阅读: [JavaScript |导入和导出模块](https://www.geeksforgeeks.org/javascript-importing-and-exporting-modules/)。

给定一个文本文件，编写一个 JavaScript 程序来提取该文件的内容。NodeJs 中有一个内置的模块或内置的库，它处理所有被称为文件系统的读取操作。它基本上是一个 JavaScript 程序(fs.js)，其中编写了用于读取操作的函数。在程序中导入 fs 模块，并使用函数从系统文件中读取文本。

**已用功能:**读取文件()功能用于读取操作。

**语法:**

```
readFile( Path, Options, Callback)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Path:** It adopts the relative path from the program to the text file. If the file and the program are in the same folder, just give the file name of the text file.
*   **Option:** It is an optional parameter that specifies the data to be read from the file. If nothing is passed, the default original buffer is returned.
*   **Callback function:** Callback function also has two parameters (err, data). If the operation cannot extract the data, err will display an error, otherwise the data parameter will contain the data in the file.

假设有一个名为 *Input.txt* 的文件和 JavaScript 程序在同一个文件夹中。

*   **Input.txt file:** This is some data in the file input.txt.
*   **剧本。js:**

    ```
    <script>
    // Requiring fs module in which 
    // readFile function is defined.
    const fs = require('fs')

    fs.readFile('Input.txt', (err, data) => {
        if (err) throw err;

        console.log(data.toString());
    })
    </script>
    ```

*   Instead of using tostring function to convert buffer into text, directly convert data into text format.

    ```
    <script>
    // Requiring fs module in which
    // readFile function is defined.
    const fs = require('fs')

    // Reading data in utf-8 format
    // which is a type of character set.
    // Instead of 'utf-8' it can be 
    // other character set also like 'ascii'
    fs.readFile('Input.txt', 'utf-8', (err, data) => {
        if (err) throw err;

        // Converting Raw Buffer to text
        // data using tostring function.
        console.log(data);
    })
    </script>
    ```

**输出:**

```
This is some data inside file Input.txt.
```

**注意:**要运行脚本，首先将两个文件放在同一个文件夹中，然后使用终端中的 NodeJs 解释器运行 script.js。