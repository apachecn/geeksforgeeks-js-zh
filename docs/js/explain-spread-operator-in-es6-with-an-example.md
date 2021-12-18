# 用一个例子解释 ES6 中的扩展运算符

> 原文:[https://www . geesforgeks . org/explain-spread-operator-in-es6-带示例/](https://www.geeksforgeeks.org/explain-spread-operator-in-es6-with-an-example/)

在本文中，我们将借助 ES6 中的某些示例，尝试了解与 spread 运算符相关的基本细节，包括 Spread 运算符的语法及其用法。

让我们首先了解什么是 Spread Operator，它的语法是什么，然后我们将看到一些与它的声明相关的例子。

**[传播算子:](https://www.geeksforgeeks.org/javascript-spread-operator/)**

*   spread 运算符最终获取任何可迭代对象，如数组或任何其他可迭代对象，并分别扩展该可迭代对象的值。
*   此扩展运算符主要用于包含 1 个以上值的数组。
*   也就是说，它基本上展开了一个数组的所有元素，而且在展开数组元素之后，我们可以对这些元素执行任何操作，比如串联，将一个数组的元素复制到另一个数组中，等等。
*   扩展运算符也可以与对象一起用于多种操作，如将一个对象的值串联或复制到另一个对象中，等等。

**语法:**遵循语法，我们可以使用任何可迭代对象(如数组)来实现 spread 运算符。

```
let variable = [...values]; 
```

基本上，这个语法所做的是从一个数组中获取值，并将其存储在一个变量中，因此这个变量本身就是一个数组。

既然我们已经了解了 spread 运算符的基本知识，包括它的语法，现在是时候看几个基于 Spread 运算符用法的例子了。

**示例 1:** 在本例中，我们将尝试首先使用 concat()方法执行连接，然后使用更简单的方法，即使用 spread 运算符。

## java 描述语言

```
<script>
    let array1 = [5, 6, 7];
    let array2 = [8, 9, 10];

    // Using concat() method.....
    let concatenatedArray = array1.concat(array2);
    console.log(concatenatedArray);

    // Using spread (...) operator......
    let newArray = [...array1, ...array2];
    console.log(newArray);
</script>
```

**输出:**正如您在上面的代码片段中看到的，通过使用扩展运算符语法而不是使用预定义的方法 concat()来执行连接变得非常简单。

```
[ 5, 6, 7, 8, 9, 10 ]
[ 5, 6, 7, 8, 9, 10 ]
```

**示例 2:** 在本例中，我们将尝试将一个数组的值复制到另一个数组中，然后我们将尝试向新数组中添加更多的值，然后我们将进一步看到更改对以前和新数组元素的影响。

## java 描述语言

```
<script>
    let arr = ["Apple", "Mango", "Banana"];
    let newArr = [...arr];

    console.log(newArr);  // [ 'Apple', 'Mango', 'Banana' ]
    newArr.push("Grapes");

    console.log(newArr);  // [ 'Apple', 'Mango', 'Banana', 'Grapes' ]
    console.log(arr);  // [ 'Apple', 'Mango', 'Banana' ]
</script>
```

**输出:**在上面的例子中可以看到，当我们在新数组中正常输入一个新值时，它不会影响旧数组，如果我们尝试用常规方法，我们可能会得到与旧数组元素相同的新数组元素。

```
[ 'Apple', 'Mango', 'Banana' ]
[ 'Apple', 'Mango', 'Banana', 'Grapes' ]
[ 'Apple', 'Mango', 'Banana' ]
```

**示例 3:** 在本例中，我们将尝试使用 spread 运算符来查找元素数组中的最小元素。

## java 描述语言

```
<script>
    let Array = [5, 6, 8, 1, 0, -8, 10];

    console.log(Math.min(...Array));
</script>
```

**输出:**如果我们试图用一些更简单的方法找到最小元素，那么我们可能会遇到一条错误消息，上面写着 NaN(不是一个数字)，但是通过使用一个扩展运算符，我们将不会得到这样的错误消息。

```
-8
```