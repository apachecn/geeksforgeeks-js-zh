# ES6 中的数组辅助方法

> 原文:[https://www.geeksforgeeks.org/array-helper-methods-in-es6/](https://www.geeksforgeeks.org/array-helper-methods-in-es6/)

ES6 (JavaScript)中的数组助手方法对于处理存储在数组中的数据非常有用。作为一名 web 开发人员，大部分时间都在处理存储在数组中的数据，它可能是一个简单的数字数组，也可能是一个复杂的对象数组，其中每个对象都包含许多属性。数组助手方法在使用数组时有很大帮助。数组助手方法可以非常容易地用于复杂的数组任务，也可以很容易地处理复杂的对象数组。

**forEach():**forEach()函数用于遍历数组的所有条目。
**例:**求一组数字中所有数字的和。

```
<script>
let sum = 0;
const numbers = [1, 2, 3, 4, 5];

numbers.forEach( (num) => {
  sum = sum + num;
});

document.write(sum); // 15
</script>
```

**输出:**

```
15
```

**map():**map()方法用于迭代数组的所有条目，修改它们并返回一个新数组，但不操作旧数组。
**示例:**将数组的每个数字乘以 2，生成一个新数组。

```
<script>
const numbers = [1, 2, 3, 4, 5];

let double = numbers.map( (num) => {

  // Its mandatory to have a
  // return while using map
  return num * 2;
});

document.write(double); // [2, 4, 6, 8, 10]
</script>
```

**输出:**

```
2, 4, 6, 8, 10
```

**示例:**map()方法也可以用于从对象数组中提取属性，并将其存储在另一个数组中。

```
<script>
const objects = [
    {a:1, b:2},
    {a:3, b:4},
    {a:5, b:6}
];

let onlybs = objects.map( (object) => {
    return object.b;
});

document.write(onlybs); // [2, 4, 6]
</script>
```

**输出:**

```
2, 4, 6
```

**filter():**filter()方法用于迭代数组的所有条目，并将所需的实体过滤到另一个数组中。
**示例:**过滤标志为 1 的所有对象。

```
<script>
let objects = [
    {flag:1, a:1},
    {flag:0, a:2},
    {flag:1, a:3}
];

// Use filter() function to
// filter the object
objects.filter((object) => {

    if(object.flag === 1) {

        // Display the result
        console.log("flag:" + object.flag
                    + ", a:" + object.a);
    }
});

</script>
```

**输出:**

```
flag:1, a:1
flag:1, a:3
```

**find():**find()方法用于迭代数组的所有条目，并返回与特定条件匹配的记录。
**示例:**查找标志为 0 的对象。

```
<script>
let objects = [
    {flag:1, a:1},
    {flag:0, a:2},
    {flag:1, a:3}
];

// Use find() function to
// filter the object
objects.find((object) => {

    if(object.flag === 0) {

        // Display the result
        console.log("flag:" + object.flag
                    + ", a:" + object.a);
    }
});

</script>
```

**输出:**

```
flag:0, a:2
```

**注意:**filter()方法返回对象数组，find()方法返回单个对象。