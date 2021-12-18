# 使用 JavaScript 计算关联数组的长度

> 原文:[https://www . geeksforgeeks . org/使用 javascript 计算关联数组的长度/](https://www.geeksforgeeks.org/calculate-the-length-of-an-associative-array-using-javascript/)

**关联数组:**在 JavaScript 中，我们有普通数组，其中一个元素出现在特定的索引处。而**关联数组**基本上是 JavaScript 中的**对象**，其中索引被用户定义的键替换。基本上，我们可以说它存储了**键值**对。

**语法:**

```
let arr = { key1: 'value'1, key2: 'value2', key3: 'value3'}
```

这里，arr 是关联数组，key1、key2 和 key3 是它的索引，value1、value2 和 value3 是它的元素。

**示例:**

```
let arr = {"apple": 10, "grapes": 20};
```

## java 描述语言

```
<script>
    let arr = {
        "apple": 10,
        "grapes": 20
    };
    arr["guava"] = 30;
    arr["banana"] = 40;
    document.writeln("Apple = " + arr.apple)
    document.write("Banana = " + arr.banana)
</script>
```

**输出:**

```
Apple = 10 Banana = 40
```

**关联数组的长度:**与普通数组一样，关联数组没有长度属性。所以我们将看到计算关联数组长度的其他方法。

为了计算关联数组的长度，我们将遍历数组元素，并计算数组中存在的所有键。

## java 描述语言

```
<script>

    // Function to calculate the
    // length of an array
    sizeOfArray = function (array) {

        // A variable to store
        // the size of arrays
        let size = 0;

        // Traversing the array
        for (let key in array) {

            // Checking if key is present
            // in arrays or not
            if (array.hasOwnProperty(key)) {
                size++;
            }
        }

        // Return the size
        return size;
    }

    // Driver code
    let arr = { "apple": 10, "grapes": 20 };
    arr["guava"] = 30;
    arr["banana"] = 40;

    // Printing the array
    console.log(arr);

    // Printing the size
    console.log("size = " + sizeOfArray(arr));

    // Adding another element to array
    arr["fruits"] = 100;

    // Printing the array and size again
    console.log(arr);
    console.log("Size = " + sizeOfArray(arr));
</script>
```

**输出:**

```
{apple: 10, grapes: 20, guava: 30, banana: 40}
size = 4
{apple: 10, grapes: 20, guava: 30, banana: 40, fruits: 100}
Size = 5
```

**使用键方法:****键()**方法返回一个包含关联数组中所有键的数组。因此，我们可以使用这个数组的 length 属性来获得关联数组的长度。

## java 描述语言

```
<script>
    let arr = { "apple": 10, "grapes": 20 };
    arr["guava"] = 30;
    arr["banana"] = 40;

    // Printing the array
    // returned by keys() method
    console.log(Object.keys(arr))

    // printing the size
    console.log("Size = " + Object.keys(arr).length)
</script>
```

**输出:**

```
['apple', 'grapes', 'guava', 'banana']
Size = 4
```