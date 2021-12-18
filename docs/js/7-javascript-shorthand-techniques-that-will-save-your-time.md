# 7 种节省你时间的 JavaScript 速记技术

> 原文:[https://www . geesforgeks . org/7-JavaScript-速记-技巧-节省时间/](https://www.geeksforgeeks.org/7-javascript-shorthand-techniques-that-will-save-your-time/)

在本文中，我们将讨论 JavaScript 中 7 个很酷的速记技巧，它们将节省开发人员的时间。

**1。箭头函数:**在 ES6 中引入了 JavaScript 箭头函数。这个函数的主要优点是，它有更短的语法。

## java 描述语言

```
// Longhand 
function add(a, b) { 
   return a + b; 
} 

// Shorthand 
const add = (a, b) => a + b;
```

**2。多行字符串:**对于多行字符串，我们通常使用+运算符和新的行转义序列(\n)。我们可以通过使用倒勾(`)以更简单的方式来实现。

## java 描述语言

```
// Longhand 
console.log('JavaScript is a lightweight, interpreted, '
    + 'object-oriented language\nwith first-class '
    + 'functions, and is best known as the scripting '
    + 'language for Web \npages, but it is used in many'
    + 'non-browser environments as well.\n'); 

// Shorthand 
console.log(`JavaScript is a lightweight, interpreted, 
object-oriented language with first-class functions, 
and is best known as the scripting language for Web 
pages, but it is used in many non-browser environments 
as well.`);
```

**3。For 循环:**要循环一个数组，我们通常使用传统的 for 循环。我们可以利用循环的*来迭代数组。要访问每个值的索引，我们可以使用*进行循环。**

## java 描述语言

```
let myArr = [50, 60, 70, 80]; 

// Longhand 
for (let i = 0; i < myArr.length; i++) { 
  console.log(myArr[i]); 
} 

// Shorthand 
// 1\. for of loop 
for (const val of myArr) { 
  console.log(val); 
} 

// 2\. for in loop 
for (const index in myArr) { 
  console.log(`index: ${index} and value: ${myArr[index]}`); 
}
```

**4。将字符串转换为数字:**有内置的方法，如**解析器**和**解析器**可用于将字符串转换为数字。也可以简单地在字符串值前面提供一元运算符(+)。

## java 描述语言

```
// Longhand 
let a = parseInt('764'); 
let b = parseFloat('29.3'); 

// Shorthand 
let a = +'764'; 
let b = +'29.3';
```

**5。互换两个变量**

为了交换两个变量，我们经常使用第三个变量。但是它可以很容易地用数组去结构赋值来完成。

## java 描述语言

```
//Longhand
let x = 'Hello', y = 'World';  
const temp = x; 
x = y; 
y = temp; 

//Shorthand 
[x, y] = [y, x];
```

**6。数组合并:**要合并两个数组，可以使用以下方法:

## java 描述语言

```
// Longhand 
let a1 = [2, 3]; 
let a2 = a1.concat([6, 8]); 

// Output: [2, 3, 6, 8] 

// Shorthand 
let a2 = [...a1, 6, 8]; 

// Output: [2, 3, 6, 8]
```

**7。** **多条件检查:**对于多值匹配，我们可以将所有值放在数组中，并使用 indexOf()或 includes()方法。

## java 描述语言

```
// Longhand 
if (value === 1 || value === 'hello' || value === 2 || value === 'world') { 
    ...
} 

// Shorthand 1
if ([1, 'hello', 2, 'world'].indexOf(value) >= 0) { 
    ... 
}

// Shorthand 2
if ([1, 'hello', 2, 'world'].includes(value)) { 
    ... 
}
```