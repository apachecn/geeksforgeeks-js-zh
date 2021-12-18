# 排版|数组映射()方法

> 原文:[https://www.geeksforgeeks.org/typescript-array-map-method/](https://www.geeksforgeeks.org/typescript-array-map-method/)

**Array.map()** 是一个内置的 [**TypeScript**](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 函数，用于创建一个新的数组，其结果是对该数组中的每个元素调用一个提供的函数。

**语法:**

```
array.map(callback[, thisObject])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **回调:**该参数是从当前数组的元素中产生新数组的元素的函数。
*   **thisObject :** 此参数是执行回调时用作此的对象。

**返回值:**这个方法返回创建的数组。

下面的例子说明了 TypeScript 中的**数组映射()**方法。
T3】例 1:

## Java Script 语言

```
// language is TypeScript

    // Driver code
    var arr = [ 11, 89, 23, 7, 98 ];

    // use of map() method
    var val = arr.map(Math.log)

    // printing element
    console.log( val );
```

**输出:**

```
[ 2.3978952727983707,
  4.48863636973214,
  3.1354942159291497,
  1.9459101490553132,
  4.584967478670572 ]
```

**例 2:**

## Java Script 语言

```
// language is TypeScript

    // Driver code
    var arr = [2, 5, 6, 3, 8, 9];

    // use of map() method   

    var newArr = arr.map(function(val, index){

      // printing element
      console.log("key : ",index, "value : ",val*val);
    })
```

**输出:**

```
key :  0 value :  4
key :  1 value :  25
key :  2 value :  36
key :  3 value :  9
key :  4 value :  64
key :  5 value :  81
```