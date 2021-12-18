# 如何在 JavaScript 中将字符串数组转换成数字数组？

> 原文:[https://www . geesforgeks . org/如何将字符串数组转换为 javascript 中的数字数组/](https://www.geeksforgeeks.org/how-to-convert-array-of-strings-to-array-of-numbers-in-javascript/)

在本文中，我们给出了一个字符串数组，任务是在 JavaScript 中将它转换成一个数字数组。

```
Input: ["1","2","3","4","5"]
Output: [1,2,3,4,5]

Input: ["10","21","3","14","53"]
Output: [10,21,3,14,53]
```

有两种方法可以做到这一点，如下所示:

**方法 1:数组遍历和类型转换:**在这个方法中，我们遍历一个字符串数组，并通过使用[parsent()](https://www.geeksforgeeks.org/javascript-parseint-function/)函数将其类型转换为整数，将其添加到一个新的数字数组中。

## java 描述语言

```
<script>

    // Create an array of string
    var stringArray = ["1", "2", "3", "4", "5"];

    // Create an empty array of number
    var numberArray = [];

    // Store length of array of string
    // in variable length
    length = stringArray.length;

    // Iterate through array of string using
    // for loop
    // push all elements of array of string
    // in array of numbers by typecasting
    // them to integers using parseInt function
    for (var i = 0; i < length; i++)

        // Instead of parseInt(), Number()
        // can also be used
        numberArray.push(parseInt(stringArray[i]));

    // Print the array of numbers
    console.log(numberArray);
</script>
```

**输出:**

```
[1, 2, 3, 4, 5]
```

**方法二:使用 JavaScript 的 map()方法:**在这个方法中，我们使用了 JavaScript 的[数组映射方法](https://www.geeksforgeeks.org/javascript-array-map-method/)。

## java 描述语言

```
<script>
    // Create an array of string
    var stringArray = ["10", "21", "3", "14", "53"];

    // Create a numberArray and using
    // map function iterate over it
    // and push it by typecasting into
    // int using Number
    var numberArray = stringArray.map(Number);

    // Print the array of numbers
    console.log(numberArray);
</script>
```

**输出:**

```
[10, 21, 3, 14, 53]
```