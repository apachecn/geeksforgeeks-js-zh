# 如何在 JavaScript 中将对象{}转换为键值对的数组[]？

> 原文:[https://www . geesforgeks . org/如何将对象转换为 javascript 中的键值对数组/](https://www.geeksforgeeks.org/how-to-convert-an-object-to-an-array-of-key-value-pairs-in-javascript/)

任务是使用 JavaScript 将对象{}转换为键值对的数组[]。
**简介:**对象，在 JavaScript 中，是它最重要的数据类型，构成了现代 JavaScript 的构建模块。这些对象与 JavaScript 的原始数据类型(数字、字符串、布尔、空、未定义和符号)有很大不同。对象更复杂，每个对象可能包含这些原始数据类型以及引用数据类型的任意组合，而数组是一个用于存储不同元素的单个变量。当我们想要存储元素列表并通过单个变量访问它们时，通常会用到它。

我们可以使用下面讨论的方法将对象{}转换为键值对的数组[]:
**方法 1:** 在此方法中，我们将使用 [Object.keys()](https://www.geeksforgeeks.org/object-keys-javascript/) 和 [map()](https://www.geeksforgeeks.org/map-in-javascript/) 来实现这一点。

**方法:**通过使用 Object.keys()，我们从对象中提取密钥，然后将该密钥传递给 map()函数，该函数将密钥和相应的值映射为数组，如下例所述。
**语法:**

*   ```
    Object.keys(obj)
    ```

    **参数:**
    **对象:**返回可枚举属性的对象。

*   ```
    map(function callback(currentValue[, index[, array]]){
        // Return element for new_array
    }
    ```

    **参数:**
    **回调:**产生新数组元素的函数

**示例:**

```
<script> 
    // An Object
    var obj = { "1": 5, "2": 7, "3": 0, "4": 0, "5": 0 };

    // Using Object.keys() and map() function
    // to convert convert an Object {} to an 
    // Array [] of key-value pairs

    var result = Object.keys(obj).map(function (key) {

        // Using Number() to convert key to number type
        // Using obj[key] to retrieve key value
        return [Number(key), obj[key]];
    });

    // Printing values
    for(var i = 0; i < result.length; i++) {
        for(var z = 0; z < result[i].length; z++) {
            document.write(result[i][z] + " ");
        }
        document.write("</br>");
    }

</script> 
```

**输出:**

```
1 5
2 7
3 0
4 0
5 0
```

**方法 2:** 在这个方法中，我们将使用 [Object.entries()](https://www.geeksforgeeks.org/object-entries-javascript/) 来实现这一点。
**方法:**我们将使用 Object.entries()，它在 JavaScript 中可用。Object.entries()方法用于返回由作为参数传递的对象的可枚举属性[键，值]对组成的数组。属性的顺序与手动循环对象属性值的顺序相同。

**语法:**

```
Object.entries(obj)
```

**参数:**
**对象:**是要返回其可枚举自身属性[键，值]对的对象。

**示例:**

```
<script> 
    // An Object
    var obj = { "1": 500, "2": 15, "5": 4, "4": 480, "10": 87 };

    // Using Object.entries() function
    // to convert convert an Object {} to an 
    // Array [] of key-value pairs
    var result = Object.entries(obj);

    // Printing values
    for(var i = 0; i < result.length; i++) {
        for(var z = 0; z < result[i].length; z++) {
            document.write(result[i][z] + " ");
        }
        document.write("</br>");
    }

</script>                    
```

**输出:**

```
1 500
2 15
4 480
5 4
10 87
```