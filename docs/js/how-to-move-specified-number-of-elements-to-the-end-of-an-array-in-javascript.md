# 如何在 JavaScript 中将指定数量的元素移动到数组末尾？

> 原文:[https://www . geesforgeks . org/如何将指定数量的元素移动到 javascript 数组末尾/](https://www.geeksforgeeks.org/how-to-move-specified-number-of-elements-to-the-end-of-an-array-in-javascript/)

本文的目的是使用 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 将一些指定的元素移动到数组的末尾。

给定一个长度为 N 的数组，将指定数量的元素 X 移动到给定数组的末尾。

**输入:**

```
arr = [1, 2, 3, 4, 5]
X = 2
```

**输出:**当前两个数字移动到数组末尾时，下面的数组应该是输出。

```
 [3, 4, 5, 1, 2]
```

**方法 1:**

*   首先，我们将从数组中提取第一个 X 元素到一个新的数组 *arr1* 中。
*   然后将数组中最后(N-X)个元素提取到新的数组 *arr2* 中。
*   然后在*之后连接*arr 1*arr 2*得到结果数组。

**JavaScript 代码:**

## java 描述语言

```
function moveElementsToEndOfArray(arr, x) {

    // arr is the input array
    // x is the no. of elements that 
    // needs to be moved to end of 
    // the array

    let n = arr.length;

    // if x is greater than length 
    // of the array
    x = x % n;

    let first_x_elements = arr.slice(0, x);

    let remaining_elements = arr.slice(x, n);

    // Destructuring to create the desired array
    arr = [...remaining_elements, ...first_x_elements];

    console.log(arr);
}

let arr = [1, 2, 3, 4, 5, 6];
let k = 5;
moveElementsToEndOfArray(arr, k);
```

**输出:**

```
[ 6, 1, 2, 3, 4, 5 ]
```

**方法 2:**

*   从索引 i = 0 到 X-1 运行 循环的[](https://www.geeksforgeeks.org/javascript-for-loop/)
*   *在每次迭代中，获取当前索引处的元素，并将其追加到数组的末尾。*
*   *迭代完成后，使用 JavaScript [*拼接()*](https://www.geeksforgeeks.org/javascript-array-splice-method/) 方法从数组中移除第一个 X 元素，得到结果数组。*

***JavaScript 代码:***

## *java 描述语言*

```
*function moveElementsToEndOfArray(arr, x) {

    // Array is [1, 2, 3, 4, 5] and x = 2
    // final output would be [3, 4, 5, 1, 2]
    x = x % (arr.length);

    for (let i = 0; i < x; i++) {
        arr.push(arr[i]);
    }

    // After this loop array will 
    // be [1, 2, 3, 4, 5, 1, 2]
    arr.splice(0, x);

    // Splice method will remove first
    // x = 2 elements from the array
    // so array will be [3, 4, 5, 1, 2]

    console.log(arr);
}

let arr = [1, 2, 3, 4, 5];
let k = 2;
moveElementsToEndOfArray(arr, k);*
```

***输出:***

```
*[ 3, 4, 5, 1, 2 ]*
```