# JavaScript 课程| JavaScript 中的数据类型

> 原文:[https://www . geesforgeks . org/JavaScript-course-data-type-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-data-types-in-javascript/)

**上一篇:** [JavaScript 课程| JavaScript 中的变量](https://www.geeksforgeeks.org/javascript-course-variables-in-javascript/)

**JavaScript 中的数据类型**

主要有两种语言。首先，一种是**静态类型语言**，其中每个变量和表达式类型在编译时都是已知的。一旦变量被声明为某个数据类型，它就不能保存其他数据类型的值。例子:C，C++，Java。

```
// Java(Statically typed)
// variable x is of type int and it
// will not store any other type.
int x = 5;

// type string and will only accept string values
string y = 'abc'; 
```

其他，**动态类型语言**:这些语言随着时间的推移可以接收不同的数据类型。例如——Ruby、Python、JavaScript 等。

```
// Javascript(Dynamically typed)
var x = 5; // can store an integer
var name = 'string'; // can also store a string.
```

JavaScript 是动态类型(也称为松散类型)脚本语言。也就是说，在 javascript 中，变量可以随着时间的推移接收不同的数据类型。数据类型基本上是可以在程序中使用和操作的数据类型。JavaScript 中的变量可以包含任何数据。这意味着一个变量在某个时候可以是一个数字，在另一个时候可以是一个字符串。

**最新的 ECMAScript(ES6)标准定义了七种数据类型**:其中六种数据类型为 Primitive(预定义)。

*   **数字** : 5、6.5、7 等。
*   **字符串**:“你好 GeeksforGeeks”等。
*   **布尔**:表示一个逻辑实体，可以有两个值:真或假。
*   **空**:该类型只有一个值:*空。*
*   **未定义**:未赋值的变量为*未定义。*
*   **对象**:它是最重要的数据类型，构成了现代 JavaScript 的构建模块。我们将在后续文章中详细了解这些数据类型。

**一个数字**
JavaScript 中的数字类型包含整数和浮点数。除了这些数字之外，我们在 javascript 中还有一些“特殊数字”，它们是:“Infinity”、“Infinity”和“NaN”。无穷大基本上代表数学上的“？”。“NaN”表示计算错误。

```
let num = 2; // integer 
let num2 = 1.3; // floating point number
let num3 = Infinity; // Infinity
let num4 = 'something here too'/2; // NaN

```

**字符串**
JavaScript 中的字符串基本上是一系列用引号括起来的字符。Javascript 中有三种类型的引号，它们是:

```
let str = "Hello There";
let str2 = 'Single quotes works fine';
let phrase = `can embed ${str}`;

```

javascript 中的单引号和双引号没有区别。Backticks 提供了额外的功能，因为在它们的帮助下，我们可以在其中嵌入变量。

```
let name = "Mukul";

// embed a variable
alert( `Hello, ${name}!` ); // Hello, Mukul!

```

**一个布尔**
这个布尔类型只有两个值:真和假。

此数据类型用于存储是/否值:true 表示“是，正确”，false 表示“否，不正确”。

```
 let isCoding = true; // yes
 let isOld = false; // no

```

**空值**
特殊的空值不属于任何默认数据类型。它形成了一个单独的类型，只包含空值:

```
let age = null;
```

“null”数据类型基本上定义了一个表示“nothing”、“empty”或“value unknown”的特殊值。

**Undefined**
就像 null 一样，Undefined 也有自己的类型。undefined 的意思是“没有赋值”。

```
let x;
console.log(x); // undefined

```

**物体**
物体本质上并不原始，理解起来有点复杂。javascript 中的所有东西基本上都是一个对象，这就是为什么很好地理解它们是什么变得非常重要的原因。对象用于存储各种数据和更复杂实体的键控集合。
我们可以通过多种方式创建对象。一种是通过使用带有可选属性列表的方括号{…}。对象的属性采用“键:值”对的形式。另一种方法是使用“new”关键字。
可以使用以下语法创建一个空对象。

```
let person = new Object(); // "object constructor" syntax
let person = {};  // "object literal" syntax

```

这两种方法都是正确，尽管选择什么完全由你决定。我们还可以将属性放入对象中，如:

```
<script>
// an object
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
</script>
```

**下一篇:** [JavaScript 课程| JavaScript 中的操作符](https://www.geeksforgeeks.org/javascript-course-operators-in-javascript/)