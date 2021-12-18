# 如何在 JavaScript 中存储一个 key= >值数组？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中存储键值数组/](https://www.geeksforgeeks.org/how-to-store-a-key-value-array-in-javascript/)

我们给出了两个包含键和值的数组，任务是在 JavaScript 中以**键= >** 值的形式将其存储为单个实体。在 JavaScript 中，数组是用于存储不同元素的单个变量。它通常在我们需要存储零件列表并通过一个变量访问它们时使用。我们可以使用下面讨论的方法在 JavaScript 对象中存储 key = >值数组:

**方法 1:** 在这个方法中，我们将使用[对象](https://www.geeksforgeeks.org/objects-in-javascript/)在 JavaScript 中存储 key = >值。对象，在 JavaScript 中，是最重要的数据类型，构成了现代 JavaScript 的构建块。这些对象与 JavaScript 的原始数据类型(数字、字符串、布尔、空、未定义和符号)有很大不同。对象更复杂，每个对象可能包含这些原始数据类型以及引用数据类型的任意组合。

**方法:**我们将遍历整个数组，并将来自键(数组)的键和来自对象中值(数组)的相应值逐一相加。

**语法:**

```
for(var i = 0; i < keys.length; i++){
        // obj = Object
        // keys = key array
        // values = value array
        obj[keys[i]] = values[i];
}

```

**例:**

```
<script> 
    // An array of keys
    var keys = [1, 2, 3];

    // An array of values
    var values = ["GeeksforGeeks", "Computer", "Science"];

    // Object created
    var obj = {};

    // Using loop to insert key
    // value in Object
    for(var i = 0; i < keys.length; i++){
        obj[keys[i]] = values[i];
    }

    // Printing object
    for (var key of Object.keys(obj)) {
        document.write(key + " => " + obj[key] + "</br>")
    }

</script>               
```

**输出:**

```
1 => GeeksforGeeks
2 => Computer
3 => Science
```

**方法 2:** 在这个方法中，我们将使用[地图](https://www.geeksforgeeks.org/map-in-javascript/)在 JavaScript 中存储 key = >值。映射是元素的集合，其中每个元素都存储为键和值对。地图对象可以将对象和基本值作为键或值保存。当我们迭代 map 对象时，它会以与插入时相同的顺序返回键、值对。

**方法:**我们将遍历整个数组，并将来自键(数组)的键和来自值(数组)的相应值逐一添加到地图中。

**语法:**

```
for(var i = 0; i < keys.length; i++){
        // mp = Map
        // keys = key array
        // values = value array
        map.set(keys[i], values[i];
}

```

**例:**

```
<script> 
    // An array of keys
    var keys = [5, 2, 3, 6, 10];

    // An array of values
    var values = ["Geeks", "for", "Geeks", "Course", "Algorithm"];

    // Map created
    var map = new Map();

    // Using loop to insert key
    // value in map
    for(var i = 0; i < keys.length; i++){
        map.set(keys[i], values[i]);
    }

    // Printing
    for (var key of map.keys()) {
        document.write(key + " => " + map.get(key) + "</br>")
    }

</script>                    
```

**输出:**

```
5 => Geeks
2 => for
3 => Geeks
6 => Course
10 => Algorithm
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。