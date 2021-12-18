# 是 6 |阵列

> 原文:[https://www.geeksforgeeks.org/es6-array/](https://www.geeksforgeeks.org/es6-array/)

数组是值的同构集合。它是用于存储不同元素的单个变量。当我们想要存储一个元素列表并通过一个变量来访问它们时，通常会用到它。与大多数语言中数组是对多个变量的引用不同，ES6 数组是存储多个元素的单个变量。我们可以使用正常变量(v1，v2，v3，..)当我们有少量对象时，但是如果我们想要存储大量实例，那么用普通变量来管理它们就变得很困难。数组的思想是在一个变量中表示多个实例。
**阵的特点:**

*   数组中有索引，因此可以使用数组索引随机访问元素。
*   可以使用单个变量名存储多个元素。
*   使用循环遍历数组变得很容易。
*   排序变得很容易，因为它可以通过在数组中写入更少的代码行来完成。
*   数组值可以修改或更新，但不能删除。

**初始化数组:**初始化或声明数组是小菜一碟。下面的程序实现了数组的初始化。

*   **节目:**

## java 描述语言

```
// Initializing while declaring
var JS = ["ES1", "ES2", "ES3", "ES4", "ES5", "ES6"];

// Initializing after declaring
JS[0] = "ES6";
JS[1] = "ES6";
JS[2] = "ES6";
JS[3] = "ES6";
```

**访问数组元素:**要访问任何特定的数组元素，我们需要知道该元素的索引号。数组索引号用于访问数组元素。数组的索引总是从 0 开始。

*   **节目:**

## java 描述语言

```
<script>
// Initializing while declaring
var JS= ["ES1", "ES2", "ES3", "ES4", "ES5", "ES6"];

// Accessing array element
console.log(JS[4])
console.log(JS[5])
</script>
```

*   **输出:**

```
ES5
ES6
```

**数组对象:**数组构造函数可以作为代表数组大小的数值传递，数组元素是逗号分隔的值。

*   **节目 1:**

## java 描述语言

```
<script>
var js = ["ES6", 2015, "ES8", 2017, "ES10", 2019];

// len contains the length of the array
var len = js.length;
for (var i = 0; i < len; i++)
    console.log(js[i]);

</script>                   
```

*   **输出:**

```
ES6
2015
ES8
2017
ES10
2019
```

*   **节目 2:**

## java 描述语言

```
<script>
var Geeks = new Array(6) 
for(var i = 0; i < Geeks.length; i++)
{
   Geeks[i] = (i * 2)/3
   console.log(Geeks[i])
}
</script>                                   
```

*   **输出:**

```
0
0.6666666666666666
1.3333333333333333
2
2.6666666666666665
3.3333333333333335
```

**数组方法:**ES6 中引入了很多数组方法。

<figure class="table">

| way | describe |
| --- | --- |
| [concat()](https://www.geeksforgeeks.org/javascript-array-prototype-concat-function/) | This method is used to merge two or more arrays together. |
| [隔()](https://www.geeksforgeeks.org/javascript-array-prototype-every-function/) | This function checks whether all elements in the array meet the given conditions provided by the function passed to it as a parameter. |
| [过滤器()](https://www.geeksforgeeks.org/es6-array-filter-method/) | This method creates a new array in which the elements follow or pass the given criteria and conditions. |
| [find()](https://www.geeksforgeeks.org/javascript-array-find-method/) | Filter elements by function, and return the first/all values to make them return true values. |
| [【forEach()】](https://www.geeksforgeeks.org/es6-array-foreach-method/) | This method is used to iterate over its elements and manipulate them. |
| [阵。from()](https://www.geeksforgeeks.org/javascript-array-method/) | This turns everything like array or iterable into a true array, especially when using DOM, so that other array methods such as reduce, map, filter and so on can be used. |
| [指数()](https://www.geeksforgeeks.org/javascript-array-indexof/) | This method is used to find the index of the first occurrence of the search element provided as a method parameter. |
| [join()](https://www.geeksforgeeks.org/javascript-array-join-method/) | This method is used to concatenate the elements of an array into a string. |
| [【最后一个索引（）】](https://www.geeksforgeeks.org/javascript-array-prototype-lastindexof-function/) | Search the item from the pos, or return the index or -1 if it is not found. |
| [地图()](https://www.geeksforgeeks.org/javascript-array-map-method/) | This method creates a new array by calling the function provided in each element. |
| 数组。of() | This creates an array from each parameter passed into it. |
| [pop()](https://www.geeksforgeeks.org/javascript-array-prototype-pop/) | Removes the last element from the array and returns it. |
| [推()](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/) | Adds one or more elements to the end of the array and returns the new length of the array. |
| [减少()](https://www.geeksforgeeks.org/javascript-array-reduce-method/) | The reduce () method applies a function to an accumulator and each element in the array (from left to right) to reduce it to a value -MDN. |
| [反转()](https://www.geeksforgeeks.org/javascript-array-prototype-reverse/) | Reverse the order of array elements–the first one becomes the last one, and the last one becomes the first one. |
| [换挡()](https://www.geeksforgeeks.org/javascript-array-prototype-shift/) | This method removes the first element of the array, thereby reducing the size of the original array by 1. |
| [切片()](https://www.geeksforgeeks.org/javascript-array-slice/) | Create a new array to copy the elements from the starting position to the ending position (excluding the starting position). |
| [一些()](https://www.geeksforgeeks.org/javascript-array-prototype-function/) | This method checks whether at least one of the items in the array has passed the condition. If it passes, it will return "true", otherwise it will return "false". |
| [排序()](https://www.geeksforgeeks.org/javascript-array-sort/) | This method is used to sort arrays in a given order according to the compare () function. |
| [splicing ()](https://www.geeksforgeeks.org/javascript-array-splice-method/) | These methods are used to modify the contents of an array by removing existing elements. |
| [unshift()](https://www.geeksforgeeks.org/javascript-array-prototype-unshift-function/) | This function increases the length of an existing array by increasing the number of elements in the array. |

</figure>

**注意:**在 JavaScript 中，数组使用编号索引，对象使用命名索引。