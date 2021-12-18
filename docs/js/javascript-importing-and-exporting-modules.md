# JavaScript |导入导出模块

> 原文:[https://www . geesforgeks . org/JavaScript-导入-导出-模块/](https://www.geeksforgeeks.org/javascript-importing-and-exporting-modules/)

JavaScript 模块基本上是包含在给定程序中的库。它们用于将两个 JavaScript 程序连接在一起，以调用一个程序中编写的函数，而无需在另一个程序中编写函数本身的主体。

**导入库:**意味着在程序中包含一个库，以便在该库中定义函数的使用。为此，请使用“require”函数，在该函数中传递库名及其相对路径。
**示例:**假设在文件名为 library.js 的同一个文件夹中制作一个库，然后使用 require 函数包含该文件:

```
const lib = require('./library') 
```

这将返回对该库引用。现在如果库中定义了面积函数，那么就用它作为 lib.area()。

**导出库:**JavaScript 中有一个特殊的对象叫做 module.exports，当某个程序包含或者导入这个模块(程序)时，这个对象就会暴露出来。因此，所有那些需要公开或需要可用的函数，以便在 module.exports 中定义的其他文件中使用。

**Expample :** 编写两个不同的程序，然后看看如何在给定的程序中使用库(Module)中定义的函数。在库中定义两个简单的函数，用于计算和打印具有长度和宽度的矩形的面积和周长。然后导出这些函数，以便其他程序可以在需要时导入并使用它们。

**导出模块示例:library.js**

```
<script>
// Area function
let area = function (length, breadth) {
    let a = length * breadth;
    console.log('Area of the rectangle is ' + a + ' square unit');
}

// Perimeter function
let perimeter = function (length, breadth) {
    let p = 2 * (length + breadth);
    console.log('Perimeter of the rectangle is ' + p + ' unit');
}

// Making all functions available in this
// module to exports that we have made
// so that we can import this module and
// use these functions whenever we want.
module.exports = {
    area,
    perimeter
}
</script>
```

**导入模块示例**

要导入任何模块，请使用名为“Require”的函数，该函数接受模块名称，如果是用户定义的模块，则将其相对路径作为参数并返回其引用。

*script.js* 包含上面的 JavaScript 模块(library.js)。

**Script.js**

```
<script>
// Importing the module library containing
// area and perimeter functions.
// " ./ " is used if both the files are in the same folder.
const lib =  require('./library');

let length = 10;
let breadth = 5;

// Calling the functions 
// defined in the lib module
lib.area(length, breadth);
lib.perimeter(length, breadth);
</script>
```

**输出:**

```
Area of the rectangle is 50 square unit
Perimeter of the rectangle is 30 unit
```

**注意:**要运行脚本，首先将两个文件放在同一个文件夹中，然后使用终端中的 NodeJs 解释器运行 script.js。