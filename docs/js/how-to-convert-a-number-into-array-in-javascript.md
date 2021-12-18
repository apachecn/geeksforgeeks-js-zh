# 如何在 JavaScript 中将一个数字转换成数组？

> 原文:[https://www . geesforgeks . org/如何将数字转换为 javascript 数组/](https://www.geeksforgeeks.org/how-to-convert-a-number-into-array-in-javascript/)

我们已经给出了一个数字，任务是使用 JavaScript 将给定的数字转换成一个数组。

**例:**

```
Input: 235283
Output: [2, 3, 5, 2, 8, 3]

Input: 8998123
Output: [8, 9, 9, 8, 1, 2, 3]

Input: 1234567
Output: [1, 2, 3, 4, 5, 6, 7]
```

在本文中，我们将使用两种不同的方法将给定的数字转换为数组。

**方法 1:使用** [**Array.from()方法**](https://www.geeksforgeeks.org/javascript-array-from-method/)**:**JavaScript**Array from()**方法从任何具有长度属性的对象或可迭代对象返回 Array 对象。

**语法:**

```
Array.from(object, mapFunction, thisValue)
```

**方法:**

1.  Store numbers in variables.
2.  Use the Array.from () method and enter the string type conversion value in its first parameter.
3.  In the second parameter, we use a function, myFunc, which will be called in every iteration.
4.  The my func function will use the Array.from () method to iterate the returned parameters. We convert the numeric type to a string, so the parameter type is a string, but we will convert its type to an integer and return it.
5.  The value returned by array. from () is our result.

**例:**

## Javascript

```
var myInt = 235345;

// Getting the string as a parameter
// and typecasting it into an integer
let myFunc = num => Number(num);

var intArr = Array.from(String(myInt), myFunc);

// Print the result array
console.log(intArr);
```

**输出:**

```
[2, 3, 5, 3, 4, 5 ]
```

**方法 2:使用** [**map()方法**](https://www.geeksforgeeks.org/javascript-array-map-method/)**:**JavaScript 中的 **map()** 方法通过对父数组中的每个元素调用特定的函数来创建数组。这是一种非突变方法。通常， **map()** 方法用于迭代数组，并对数组的每个元素调用一个函数。

**语法:**

```
array.map(function(currentValue, index, arr), thisValue)
```

**方法:**

1.  Store integer values in variables.
2.  Type an integer into a string.
3.  Use the split () method to make it an array of strings.
4.  Iterate the array using the map () method.
5.  Use the map () method to return a string array to an integer array.

## Javascript

```
// Declare a variable and store an
// integer value
var num = 235345

// Here we typecasting the num
// Splitting the num, so that
// we got an array of strings
// Then use map function to
// convert the array of strings
// into array of numbers

var myArr = String(num).split("").map((num)=>{
  return Number(num)
})

console.log(myArr)
```

**输出:**

```
[2, 3, 5, 3, 4, 5]
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。