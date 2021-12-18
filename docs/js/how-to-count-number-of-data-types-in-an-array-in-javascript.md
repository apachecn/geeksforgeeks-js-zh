# 如何在 JavaScript 中统计数组中数据类型的个数？

> 原文:[https://www . geesforgeks . org/如何计算 javascript 数组中的数据类型数/](https://www.geeksforgeeks.org/how-to-count-number-of-data-types-in-an-array-in-javascript/)

给定一个数组，任务是计算用于创建该数组的数据类型的数量。

**示例:**

> **输入:【T11，真】、【hello】、[]、{}、undefined、function(){}】
> **输出:** {
> 布尔:1、
> 函数:1、
> 数字:1、
> 对象:2、
> 字符串:1、
> undefined: 1
> }
> **输入:**【function(){ }、new Object()、[]、{ }、NaN、Infinity、undefined、null、0】**

strong >方法 1:在这种方法中，我们使用 [Array.reduce()方法](https://www.geeksforgeeks.org/javascript-array-reduce-method/)并用一个空对象初始化该方法。

## java 描述语言

```
<script>
// JavaScript program to count number of data types in an array
let countDtypes = (arr) => {
    return arr.reduce((acc, curr) => {

            // Check if the acc contains the type or not
            if (acc[typeof curr]) {

                // Increase the type with one
                acc[typeof curr]++;
            } else {

                /* If acc not contains the type
                then initialize the type with one */
                acc[typeof curr] = 1
            }
            return acc
        }, {}) // Initialize with an empty array
}

let arr = [function() {}, new Object(), [], {},
 NaN, Infinity, undefined, null, 0];

console.log(countDtypes(arr));
</script>
```

**输出:**

```
{
   function: 1,
   number: 3,
   object: 4,
   undefined: 1
}
```

**方法 2:** 在这种方法中，我们使用 [Array.forEach()方法](https://www.geeksforgeeks.org/javascript-array-foreach-method/)来迭代数组。创建一个空数组，在每次迭代时，我们检查当前迭代的类型是否存在于新创建的对象中。如果是，那么就用 1 增加类型，否则用类型的名称创建一个新的键，并用 1 初始化。

## java 描述语言

```
<script>
// JavaScript program to count number of data types in an array
let countDtypes = (arr) => {
    let obj = {}

    arr.forEach((val) => {

        // Check if obj contains the type or not
        if (obj[typeof val]) {

            // Increase the type with one
            obj[typeof val]++;
        } else {

            // Initialize a key (type) into obj
            obj[typeof val] = 1;
        }
    })
    return obj
}

let arr = [function() {}, new Object(), [], {},
    NaN, Infinity, undefined, null, 0
];

console.log(countDtypes(arr));
</script>
```

**输出:**

```
{
  boolean: 1,
  function: 1,
  number: 1,
  object: 2,
  string: 1,
  undefined: 1
}
```