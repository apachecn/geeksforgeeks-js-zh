# 如何在 JavaScript 中将二维数组转换成对象？

> 原文:[https://www . geesforgeks . org/如何将二维数组转换为 javascript 中的对象/](https://www.geeksforgeeks.org/how-to-convert-two-dimensional-array-into-an-object-in-javascript/)

在本文中，我们将学习如何将[二维数组](https://www.geeksforgeeks.org/multidimensional-array-in-javascript/)转换为[对象](https://www.geeksforgeeks.org/objects-in-javascript/)。二维数组可以有任意数量的行和两列。

**示例:**

```
Input: [
         ["John", 12],
         ["Jack", 13],
         ["Matt", 14],
         ["Maxx", 15]
       ]

Output: {
"John": 12,
          "Jack": 13,
          "Matt": 14,
          "Maxx": 15
        }
```

可以遵循以下方法来解决问题。

**方法 1:** 在这种方法中，我们创建一个空对象，并使用 **Array.forEach()** 方法迭代数组。在每次迭代中，我们将子数组的第一项作为键插入到对象中，第二项作为值插入。然后它在迭代后返回对象。

**示例:**

## java 描述语言

```
function arr2obj(arr) {

    // Create an empty object
    let obj = {};

    arr.forEach((v) => {

        // Extract the key and the value
        let key = v[0];
        let value = v[1];

        // Add the key and value to
        // the object
        obj[key] = value;
    });

    // Return the object
    return obj;
}

console.log(
    arr2obj([
        ["John", 12],
        ["Jack", 13],
        ["Matt", 14],
        ["Maxx", 15],
    ])
);
```

**输出:**

```
{
  Jack: 13,
  John: 12,
  Matt: 14,
  Maxx: 15
}
```

**方法 2:** 在这种方法中，我们将使用 **Array.reduce()** 方法并用一个空对象初始化累加器。在每次迭代中，我们将当前值指定为累加器的键值，并返回累加器。然后它在迭代后返回对象。

**示例:**

## java 描述语言

```
function arr2obj(arr) {
    return arr.reduce(
        (acc, curr) => {

            // Extract the key and the value
            let key = curr[0];
            let value = curr[1];

            // Assign key and value
            // to the accumulator
            acc[key] = value;

            // Return the accumulator
            return acc;
        },

        // Initialize with an empty object
        {}
    );
}

console.log(
    arr2obj([
        ["Eren", "Yeager"],
        ["Mikasa", "Ackermann"],
        ["Armin", "Arlelt"],
        ["Levi", "Ackermann"],
    ])
);
```

**输出:**

```
{
  Eren: 'Yeager',
  Mikasa: 'Ackermann',
  Armin: 'Arlelt',
  Levi: 'Ackermann'
}
```

**方法 3:** 在这种方法中，我们首先使用 **Array.flat(** )方法展平数组，这样我们就得到一个一维数组。然后，我们可以创建一个空对象，并迭代数组，将位置均匀的值指定为对象的键，将位置奇怪的值指定为值。

**示例:**

## java 描述语言

```
function arr2obj(arr) {

    // Flatten the array
    arr = arr.flat();

    // Create an empty object
    let obj = {};

    for (let i = 0; i < arr.length; i++) {
        if (i % 2 == 0) {

            // Extract the key and the value
            let key = arr[i];
            let value = arr[i + 1];

            // Assign the key and value
            obj[key] = value;
        }
    }

    return obj;
}

console.log(
    arr2obj([
        ["Max", 19],
        ["Chloe", 20],
        ["Nathan", 22],
        ["Mark", 31],
    ])
);
```

**输出:**

```
{ 
  Max: 19,
  Chloe: 20, 
  Nathan: 22, 
  Mark: 31 
}
```