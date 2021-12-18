# 什么是 JavaScript 中的导出默认值？

> 原文:[https://www . geesforgeks . org/什么是导出-默认-in-javascript/](https://www.geeksforgeeks.org/what-is-export-default-in-javascript/)

export 语句在创建 JavaScript 模块时用于从模块中导出对象、函数和变量，以便其他程序可以在 import 语句的帮助下使用它们。
出口有两种类型。一个是命名导出，另一个是默认导出。

**命名出口:**命名出口对出口几种价值有用。在导入过程中，必须使用相应对象的相同名称。

```
// Exporting individual features
export var name1 = …, name2 = …, …, nameN; // also let, const

// Export list
export { name1, name2, …, nameN };

//Exporting everything at once
export { object, number, x, y, boolean, string }

// Renaming exports
export { variable1 as name1, variable2 as name2, …, nameN };

// export features declared earlier
export { myFunction, myVariable }; 
```

**示例:**

```
//file math.js
function square(x) {
  return x * x;
}
function cube(x) {
  return x * x;
}
export { square, cube };

//while importing square function in test.js
import { square, cube } from './math;
console.log(square(8)) //64
console.log(cube(8)) //512
```

**输出:**

```
64
512

```

**默认导出:**默认导出仅用于导出单个对象、函数、变量。在导入过程中，我们可以使用任何名称进行导入。

```
// file module.js
var x=4; 
export default x;

// test.js
// while importing x in test.js
import y from './module'; 
// note that y is used import x instead of 
// import x, because x was default export
console.log(y);        
// output will be 4
```

**输出**

```
4

```

带函数的默认导出的另一个例子

```
// file math.js
export default function square(x) {
  return x * x;
}

//while importing square function in test.js
import square from './math;
console.log(square(8)) //64
```

**输出:**

```
64

```

**同时使用命名和默认导出:**可以在同一个文件中使用命名和默认导出。这意味着两者将被导入到同一个文件中。

**示例:**

```
//module.js
var x=2;
const y=4;
function fun() {
   return "This a default export."
}
function square(x) {
  return x * x;
}
export { fun as default, x, y, square };
```

在导入这个 module.js 时，我们可以使用任何名称来取乐，因为它是默认的导出，并且是其他命名导出的大括号。

```
//test.js file
import anyname, { x, y, square} from './module.js';
console.log(anyname()); //This is a default export.
console.log(x); //2
```

**输出**

```
This is a default export.
2

```