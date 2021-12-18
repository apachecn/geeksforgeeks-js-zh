# JavaScript 中的函数式编程

> 原文:[https://www . geesforgeks . org/functional-programming-in-JavaScript/](https://www.geeksforgeeks.org/functional-programming-in-javascript/)

函数式编程(FP)和编程一样古老，但我们中的一些人认为它是最近才被发现的，因为我们在数学中发现了一些部分，但在编程世界中没有。但是现在函数式编程是一种趋势。几乎每一种编程语言包括 Java、Python、JavaScript 等。采用函数式编程。现在看来函数式编程是主流。但是为什么大家都在关注函数式编程。一定有什么东西。正确的问题应该是*为什么是功能编程*？所以让我们探索一下。

一般有两种编程类型。

**命令式:**通过命令式编程，我们的代码告诉编译器和用户*如何完成*任务。

## Javascript

```
const arr = [1, 2, "3", "4", 5, 6, "7", 8, "9"];

function even(el) {
    return el % 2 === 0;
}

// Converting string to number in array
const arrAsNumbers = arr.map(function (el) {
    return Number(el);
});
// console.log( arrAsNumbers );
// or
// const arrAsNumbers = arr.map(Number);
// [1, 2, 3, 4, 5, 6, 7, 8, 9];

// Filtering even numbers
const filteredArr = arrAsNumbers.filter(function (el) {
    return even(el);
});
// or
// const filteredArr = arrAsNumbers.filter(even);

console.log(filteredArr);   // [ 2, 4, 6, 8 ]
```