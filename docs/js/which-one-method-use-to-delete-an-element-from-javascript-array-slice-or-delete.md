# 用哪一种方法从 JavaScript 数组中删除一个元素(切片还是删除)？

> 原文:[https://www . geeksforgeeks . org/使用哪一种方法从 javascript 数组中删除元素切片或删除/](https://www.geeksforgeeks.org/which-one-method-use-to-delete-an-element-from-javascript-array-slice-or-delete/)

我们可以使用这两种方法从 javascript 数组中删除一个元素。答案完全取决于应用程序和程序员。

**[**切片()法**](https://www.geeksforgeeks.org/javascript-array-slice-method/) **做什么？****

**顾名思义，slice 方法对数组进行切片，并返回新数组的副本。这个方法不影响主数组，它只是返回数组的副本。我们可以将数组的这个副本给主数组或任何其他数组，以获得切片数组。**

****语法:****

```
array.slice(arg1, arg2); 
```

****参数:**它接受以下两个参数:**

***   **arg1:** It refers to the starting index at which the method will start slicing. The starting index is inclusive, which means that if we give 0, it will start at the 0th index.*   **arg2:** refers to the endpoint index. The ending index is exclusive, which means that it will not include slices.**

**中的给定索引

没有必要给出两个参数，如果我们不提供开始索引，它将从第 0 个索引开始，如果我们不提供结束索引，它将到达最后一个索引。

**返回值:**返回新数组的副本

**示例 1:** 这里，我们给出的起始索引为 2，结束索引为 4，因此它将对元素 2、3 进行切片。如您所见，它返回新数组的副本，我们将它存储在同一个数组中。该方法还缩短了数组长度。以前数组的长度是 4，对数组进行切片后，它变成了 2。

## Javascript

```
<script>
    // Sample array
    var arr = ["super", "duper", "upar", "chopper"];

    // Printing array length before function call
    console.log(arr.length);

    // Function call
    arr = arr.slice(2, 4);

    // Printing array and its length
    // after function call
    console.log(arr, arr.length);
</script>
```

**输出:**

```
4
[ 'upar', 'chopper' ] 2
```

**示例 2:** 这里我们没有给出结束索引，所以它将从第一个索引开始，切片到最后一个。

## Javascript

```
<script>
    // Sample array
    var arr = ["super", "duper", "upar", "chopper"];

    // Printing length before function call
    console.log(arr.length);

    // Function call
    arr = arr.slice(1);

    // Printing array and its length
    // after function call
    console.log(arr, arr.length);
</script>
```**