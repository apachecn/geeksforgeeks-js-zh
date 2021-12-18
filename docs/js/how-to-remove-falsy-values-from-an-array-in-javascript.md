# 如何在 JavaScript 中移除数组中的虚假值？

> 原文:[https://www . geeksforgeeks . org/如何从 javascript 数组中移除 falsy 值/](https://www.geeksforgeeks.org/how-to-remove-falsy-values-from-an-array-in-javascript/)

**虚假值:**JavaScript 中有 7 个虚假值，如下所示

*   错误的
*   零(0，-0)
*   空字符串(“”、“”、**`)**
*   bigintzero(0 n.0x 0n)
*   空
*   不明确的
*   圆盘烤饼

在 JavaScript 中，数组接受所有类型的假值。让我们看看如何在 JavaScript 中从数组中移除虚假值的一些方法:

*   使用 for-each 循环
*   使用数组过滤器方法
*   使用数组缩减方法
*   用于…的循环

**示例:**

> 输入:[23，0，“gfg”，假，真，NaN，12，“hi”，未定义，[]，" "]
> 输出:[23，“gfg”，真，12，“hi”，[]]
> 输入:[" "，0，假，未定义，NaN，null]
> 输出:[]

**方法:**实现这一点的方法有很多，其中一些方法如下:

**用于..每个循环:**在这种方法中，我们将使用..每次循环和每次迭代，我们检查该值是否真实，如果真实，我们将该值放入新创建的数组中，然后返回新数组。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {
    // newly created array
    let newArr = [];

    // Iterate the array using the forEach loop
    arr.forEach((k) => {
      // check for the truthy value
      if (k) {
        newArr.push(k);
      }
    });
    // return the new array
    return newArr;
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```

**使用 Array.filter()方法:**在这种方法中，我们使用的是 [array.filter](https://www.geeksforgeeks.org/javascript-array-filter-method/) 方法。filter 方法检查数组，过滤掉数组的错误值，并返回一个新数组。

**示例:**

## java 描述语言

```
<script>
  let arr = ["", 0, false, undefined, NaN, null];

  function removeFalsey(arr) {
    // Applying the filter method on the array
    return arr.filter((k) => {
      // Checking if the value is truthy
      if (k) {
        return k;
      }
    });
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[]
```

**array . filter()方法的 es6 方式:**如果可以用这个 ES6 句子。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {
    // Return the first parameter of the callback function
    return arr.filter((val) => val);
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```

**传递 Bollean 值:**也可以通过传递**布尔**构造函数作为 filter 方法的参数来实现。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {
    // Passing Boolean constructor inside filter
    return arr.filter(Boolean);
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```

**使用 Array.reduce 方法:**使用 Array.reduce 方法，我们迭代数组并用空数组初始化累加器，如果当前值不是假值，那么我们返回累加器的串联值，否则我们只返回累加器。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {
    return arr.reduce((acc, curr) => {
      // Check if the truthy then return concatenated value acc with curr.
      // else return only acc.
      if (curr) {
        return [...acc, curr];
      } else {
        return acc;
      }
    }, []); // Initialize with an empty array
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```

**用于循环**的…

**使用 for…of 循环:**使用 for…of 循环迭代数组，并检查每个项目是否虚假或真实。如果该项目是真实的，则将该项目推送到新创建的数组。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {

    // Create a new array
    let output = [];
    for (x of arr) {
      if (x) {

        // Check if x is truthy
        output.push(x);
      }
    }
    return output;
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```

**使用简单 for 循环:**使用 for 循环迭代数组并检查每一项是假还是真。如果该项目是真实的，则将该项目推送到新创建的数组。

**示例:**

## java 描述语言

```
<script>
  let arr = [23, 0, "gfg", false, true, NaN, 12, "hi", undefined, [], ""];

  function removeFalsey(arr) {
    // Create a new array
    let output = [];
    for (let i = 0; i < arr.length; i++) {
      if (arr[i]) {
        output.push(arr[i]);
      }
    }
    return output;
  }

  console.log(removeFalsey(arr));
</script>
```

**输出:**

```
[23, "gfg", true, 12, "hi", []]
```