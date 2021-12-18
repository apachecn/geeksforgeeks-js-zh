# ES6 简介

> 原文:[https://www.geeksforgeeks.org/introduction-to-es6/](https://www.geeksforgeeks.org/introduction-to-es6/)

ES6 或 ECMAScript 2015 是 ECMAScript 编程语言的第 6<sup>版。ECMAScript 是 2015 年发布的 Javascript 的标准化，随后更名为 ECMAScript 2015。
ECMAScript 和 Javascript 本质上都是不同的。</sup> 

**ECMAScript vs Javascript**

**ECMAScript:** 它是 ECMA-262 中定义的用于创建通用脚本语言的规范。简单来说，这是创建脚本语言的标准化。它是由 Ecma 国际公司推出的，基本上是我们学习如何创建脚本语言的一个实现。
**Javascript:** 一种符合 ECMAScript 规范的通用脚本语言。它基本上是一个告诉我们如何使用脚本语言的实现。

**是 6**

Javascript ES6 已经存在了几年，它允许我们以一种巧妙的方式编写代码，这基本上使代码更加现代，可读性更强。公平地说，通过使用 ES6 特性，我们写得更少，做得更多，因此术语“写得更少，做得更多”绝对适合 ES6。
ES6 引入了几个关键特性，比如 const、let、箭头函数、模板文字、默认参数等等。让我们一个接一个地看一看。
**【const】和【let】**
在 ES6 之前，每当我们想要声明一个变量时，我们主要使用 var 关键字。但是它有一些严重的问题，也不是开发人员最喜欢的，所以在 ES6 版本中，我们被引入 const 和 let 关键字，允许我们存储变量。它们都有自己存储变量的方式。

**const**:const 关键字主要是用来存储那个值不会变的变量。考虑一个例子，您正在创建一个 web 应用程序，您想要存储一个其值不会改变的变量，那么*常量*绝对是存储该变量的最佳选择。在 javascript 中，const 被认为比 var 更强大。一旦用于存储变量，就不能重新分配。简单来说，它是一个*不可变的*变量，除非与对象一起使用。
**例**:

## java 描述语言

```
// Const 
const name = 'Mukul';
console.log(name); // Will print 'Mukul' to the console.

// Trying to reassign a const variable
name = 'Rahul';
console.log(name); // Will give TypeError.
```

**输出:**
![](img/f848daab6251cc7b0db23fb31dd74a76.png)在上面的代码中，我们用 const 关键字声明了一个变量名，然后 console.log 它工作正常，但是用其他值重新分配它会给出一个错误。现在让我们看一个例子，我们使用 const 关键字声明一个对象。

## java 描述语言

```
// Object using const
const person ={
    name:'Mukul Latiyan',
    age:'21',
    isPlaced:true
};

console.log(person.name); // 'Mukul Latiyan'
person.name = 'Mayank';

console.log(person.name); //'Mayank'
```

**输出:**
![](img/ff326a1a43db0e0dd94436e7767e7706.png)使用 const 关键字声明的对象的属性是可变的，就像在上面的代码中我们用一些属性声明了一个 person 对象，比如*的名字、年龄、isPlaced* 。当我们尝试访问属性时，一切都很好，当我们更改名称属性时，也很好。因此，我们得出一个结论，即使用 const 关键字声明，对象属性也是可变的。
**let** :在 let 关键字的情况下，声明的变量将是可变的，即有值可以更改。它的工作原理类似于 var 关键字，但有一些关键的区别，如作用域，与 var 相比，它是一个更好的选择。

## java 描述语言

```
// let
let name = 'Mukul';
console.log(name); // Mukul

name = 'Rahul';
console.log(name); // Rahul
```