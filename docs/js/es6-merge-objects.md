# ES6 |合并对象

> 原文:[https://www.geeksforgeeks.org/es6-merge-objects/](https://www.geeksforgeeks.org/es6-merge-objects/)

我们可以使用两种流行的方法在 ES6 中合并两个 JavaScript 对象。方法如下:

*   Object.assign()方法
*   对象扩展语法方法

下面用适当的例子描述这两种方法:
**方法 1:** 要合并两个对象，我们将使用 [Object.assign()](https://www.geeksforgeeks.org/object-assign-javascript/) 方法。

*   **语法:**

```
Object.assign(target, ...sources)
```

*   **例:**

## java 描述语言

```
<script>

    // An Object
    var obj1 = {1 : "Geeks", 2: "for"};
    var obj2 = { 3 : "Geeks"};

    // Using Object.assign()
    Object.assign(obj1, obj2);

    // Printing object
    for (var key of Object.keys(obj1)) {
        document.write(key + " => " + obj1[key] + "</br>")
    }
</script>
```

*   **输出:**

```
1 => Geeks
2 => for
3 => Geeks
```

**方法 2:** 在这个方法中，为了合并两个对象，我们将使用**对象扩展语法**。

*   **语法:**

```
var objClone = { ...obj };
```

*   **例:**

## java 描述语言

```
<script>

    // An Object
    var obj1 = {1 : "Geeks", 2: "for"};
    var obj2 = { 3 : "Geeks"};

    // Using Object spread syntax
    var obj = {...obj1, ...obj2};

    // Printing object
    for (var key of Object.keys(obj)) {
        document.write(key + " => " + obj[key] + "</br>")
    }
</script>
```

*   **输出:**

```
1 => Geeks
2 => for
3 => Geeks
```