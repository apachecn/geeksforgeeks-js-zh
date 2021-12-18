# 类型脚本数组

> 原文:[https://www.geeksforgeeks.org/typescript-arrays/](https://www.geeksforgeeks.org/typescript-arrays/)

数组是用户定义的数据类型。数组是相似类型元素的同构集合，具有连续的内存位置，可以存储不同数据类型的多个值。
数组是一种数据结构，它存储相似数据类型的元素，并将其视为一个对象。我们只能存储一组固定的元素，一旦它的大小被声明，就不能扩展它的大小。
数组遵循基于索引的存储，即数组的第一个元素存储在索引 0 或索引“I”处，其余元素存储在位置“i+1”处。
**阵的特点**

*   相同数据类型的元素存储在数组中。

*   数组元素总是存储在连续的内存位置。

*   二维数组元素的存储在一个连续的存储单元中逐行排列。

*   地址的起始元素由数组名表示。

*   数组的大小应该在初始化时声明。

*   数组的剩余元素可以通过使用数组的起始索引来检索。

Typescript 支持数组，就像在 JavaScript 中一样。在 typescript 中声明数组有两种方式:
**1。使用方括号。**T3】

```
let array_name[:datatype] = [val1, val2, valn..]  
```

**例:**

## java 描述语言

```
let fruits: string[] = ['Apple', 'Orange', 'Banana'];
```

**2。使用泛型数组类型。**
TypeScript 数组可以包含不同数据类型的元素，如下图所示。

```
let array_name: Array = [val1, val2, valn..]  
```

**例:多型阵**

## java 描述语言

```
var values: (string | number)[] = ['Apple', 2, 'Orange', 3, 4, 'Banana'];
// or
var values: Array = ['Apple', 2, 'Orange', 3, 4, 'Banana'];
```

**示例:访问数组元素**

*   数组元素的访问基于索引(即)ArrayName[index]。

## java 描述语言

```
let fruits: string[] = ['Apple', 'Orange', 'Banana'];
fruits[0]; // returns Apple
fruits[1]; // returns Orange
fruits[2]; // returns Banana
fruits[3]; // returns undefined
```

*   我们可以通过使用“FOR”循环来访问数组元素:

## java 描述语言

```
let fruits: string[] = ['Apple', 'Orange', 'Banana'];

for(var index in fruits)
{
    console.log(fruits[index]);  // output: Apple Orange Banana
}

for(var i = 0; i < fruits.length; i++)
{
    console.log(fruits[i]); // output: Apple Orange Banana
}
```

**优势**
代码优化:我们可以更高效地检索或排序数组数据。
随机访问:我们可以使用位置指针随机访问数组数据。
**缺点**
大小限制:数组的大小是固定的(即静态的)。一旦声明了数组，我们就不能增加它的大小。

**一个阵有两种类型:**
**1。单维阵**
**2。多维阵列**

**一维数组**
它是只包含一行存储数据的数组的最简单形式。它包含单组方括号(“[]”)。
**语法:**

```
let array_name[:datatype]; 
```

**初始化:**

```
array_name = [val1, val2, valn..]
```

**例:**

## java 描述语言

```
let arr:number[];  
arr = [1, 2, 3, 4]  
console.log("Array[0]: " +arr[0]);  
console.log("Array[1]: " +arr[1]); 
```

**输出:**

```
Array[0]: 1
Array[1]: 2
```

**多维数组**
数据以行和列(也称为矩阵形式)存储在多维数组中。
类型脚本数组
T5】语法:T7】

```
let arr_name:datatype[][] = [ [a1, a2, a3], [b1, b2, b3] ];  
```

**初始化:**

```
let arr_name:datatype[initial_array_index][referenced_array_index] = [ [val1, val2, val 3], [v1, v2, v3]];  
```

**例:**

## java 描述语言

```
var mArray:number[][] = [[10, 20, 30], [50, 60, 70]] ; 
console.log(mArray[0][0]); 
console.log(mArray[0][1]); 
console.log(mArray[0][2]); 
console.log(); 
console.log(mArray[1][0]); 
console.log(mArray[1][1]); 
console.log(mArray[1][2]); 
```

**输出:**T2】

```
10
20
30

50
60
70
```

**数组对象**
我们可以通过使用或初始化数组对象来创建数组。数组构造函数用于传递以下参数来创建数组:

*   表示数组大小的数值。

*   逗号分隔值的列表。

**语法:**

```
1.let arr_name:datatype[] = new Array(values);  
```

**例:**

## java 描述语言

```
// Initializing an Array by using the Array object. 
let arr:string[] = new Array("GEEKSFORGEEKS", "2200", "Java", "Abhishek"); 
for(var i = 0;i<arr.length;i++) {  
   console.log(arr[i]); 
```