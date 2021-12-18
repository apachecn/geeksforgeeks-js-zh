# JavaScript |将数据写入文本文件的程序

> 原文:[https://www . geesforgeks . org/JavaScript-程序写入文本文件中的数据/](https://www.geeksforgeeks.org/javascript-program-to-write-data-in-a-text-file/)

**先决条件:**如何在 JavaScript 中导入库。从这里阅读:https://www . geesforgeks . org/JavaScript-导入-导出-模块/。

NodeJs 中有一个内置模块或内置库，它处理所有被称为文件系统的写操作。它基本上是一个 JavaScript 程序(fs.js)，其中编写了用于写操作的函数。在程序中导入 fs-module，并使用函数将文本写入系统中的文件。下面的函数将创建一个具有给定名称的新文件，如果没有的话，它将重写该文件，擦除其中所有以前的数据。

**已用函数:**write file()函数用于写操作。

**语法:**

```
writeFile( Path, Data, Callback)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Path:** It adopts the relative path from the program to the text file. If you want to create a file in the same folder as the program, only the file name is given. If the file does not exist, a new file will be created automatically.
*   **Data:** This parameter accepts the data to be written into the file.
*   **Callback function:** is a callback function with one parameter (err). If the operation fails to write data, err will display a fault.

**例:**

```
<script>
// Requiring fs module in which
// writeFile function is defined.
const fs = require('fs')

// Data which will write in a file.
let data = "Learning how to write in a file."

// Write data in 'Output.txt' .
fs.writeFile('Output.txt', data, (err) => {

    // In case of a error throw err.
    if (err) throw err;
})
</script>
```

**输出:**

```
Learning how to write in a file.
```

**注意:**以上脚本可以在终端使用 NodeJs 解释器运行。