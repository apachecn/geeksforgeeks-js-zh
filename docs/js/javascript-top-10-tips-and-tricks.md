# JavaScript |十大技巧和诀窍

> 原文:[https://www . geesforgeks . org/JavaScript-top-10-提示和技巧/](https://www.geeksforgeeks.org/javascript-top-10-tips-and-tricks/)

![](img/544f02ef5126bc4a71e07ac5c5eb3b31.png)

对于 web 开发或者跨平台开发来说， [**JavaScript**](https://www.geeksforgeeks.org/javascript-tutorial/) 正在广泛普及。曾经它被认为只是一种前端脚本语言，但现在它也作为后端开始流行。甚至脸书的《反应原生》也是基于 JavaScript 的。因此，了解 JavaScript 中的一些技巧肯定是有益的，这些技巧不仅可以防止我们编写额外的代码行，还可以使我们的代码简洁高效。
**1。更快的数组索引:**考虑一个数组**【10，9，8，7，6】**，如果我们想将这个数组的值赋给任何变量，我们的定位方法将是 **const a =数组【0】**。如果我们想分配多个变量，继续这样做将是乏味的。

*   **代码 1:** 老派方式。

## 超文本标记语言

```
<script>
    var array1 = [10, 9, 8, 7, 6];
    var x = array1[0];
    var y = array1[1];
    var z = array1[2];
    document.write("x = " + x + "<br>");
    document.write("y = " + y + "<br>");
    document.write("z = " + z + "<br>");
</script>
```

*   **输出:**

```
x = 10
y = 9
z = 8
```

*   **代码 2:** 更聪明的方法。

## 超文本标记语言

```
<script>
    var array2 = [10, 9, 8, 7, 6];
    var [x, y, z, ...rest] = array2;
    document.write("x = " + x + "<br>");
    document.write("y = " + y + "<br>");
    document.write("z = " + z + "<br>");
    document.write("rest = " + rest + "<br>");
</script>
```

*   **输出:**

```
x = 10
y = 9
z = 8
rest = 7, 6
```

[**2。定义函数:**](https://www.geeksforgeeks.org/javascript-function-definitions/) 其思想是将一些常见的或重复的任务放在一起，并制作一个函数，这样我们就可以调用该函数，而不是针对不同的输入反复编写相同的代码。每个人一定都在 JavaScript 中使用过这样的函数。

*   **代码 1:** 以范式定义函数。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>

<p>Usual function in JavaScript</p>

    <p id="demo"></p>

    <script>
        function myFunction(p1, p2) {
            return p1 * p2;
        }
        document.getElementById("demo").innerHTML
                = myFunction(4, 3);
    </script>
</body>

</html>
```

*   **输出:**

```
Usual function in JavaScript
12
```

*   **代码 2:** 还有另一种方法，将函数视为变量，这不是一个非常有用的技巧，但仍然是新的东西。变量中的 hold 函数，它使用箭头函数，就像这样。

## java 描述语言

```
<!DOCTYPE html>
<html>

<body>

<p>
        Function treated as
        variable in JavaScript:
    </p>

    <p id="demo"></p>

    <script>
        var myFunction = (p1, p2) => {
            return p1 * p2;
        }
        document.getElementById("demo")
            .innerHTML = myFunction(4, 3);
    </script>
</body>

</html>
```

*   **输出:**

```
Function treated as variable in JavaScript
12
```

**3。在一行中定义函数:**现在这个技巧真的很酷。如果你了解 Python，你可能知道 **lambda** 函数，它表现为一个任意函数，并且用一行代码编写。嗯，我们在 JavaScript 中不使用 **lambda** 函数，但是我们仍然可以编写一行函数。假设我们想计算两个数字 **a** 和 **b** 的乘积，我们可以用一行脚本来完成。我们不需要专门编写 **return** 语句，因为这种定义方式已经意味着它会自己返回输出。

*   **代码:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<body>

<p>
        Function treated as
        variable in JavaScript
    </p>

    <p id="demo"></p>

    <script>
        const productNum = (a, b) => a * b

        document.getElementById("demo")
            .innerHTML = myFunction(4, 3);
    </script>
</body>

</html>
```

*   **输出:**

```
Function treated as variable in JavaScript
12
```

**4。布尔:**虽然每种编程语言都只有两个布尔值**真**和**假**。JavaScript 更进一步，引入了一个允许用户创建 bools 的特性。与**真**和**假**不同，它们通常分别被称为“真”和“假”。为了避免混淆，除了 **0、False、NaN、null，“**之外的所有值都默认为 Truthy。布尔函数的这种扩展使用帮助我们有效地检查条件。

*   **代码:**

## java 描述语言

```
<script>
    const a = !1;
    const b = !!!0;

    console.log(a);
    console.log(b);
</script>
```

*   **输出:**

```
False
True
```

**5。过滤布尔:**有时候我们可能想过滤掉所有的布尔，比如一个数组中的“Falsy”布尔( **0，False，NaN，null，“**)，这可以通过结合使用 [**映射**](https://www.geeksforgeeks.org/javascript-array-map-method/) 和 [**过滤器**](https://www.geeksforgeeks.org/javascript-array-filter/) 功能来完成。这里，它使用**布尔**关键字过滤掉虚假值。

*   **代码:**

## Java Script 语言

```
<script>
arrayToFilter
    .map(item => {
        // Item values
    })

    .filter(Boolean);
</script>
```

```
Input: [1, 2, 3, 0, "Hi", False, True]

Output: [1, 2, 3, "Hi", True]
```

**6。创建完全空的对象:**如果被要求在 JavaScript 中创建一个空对象，我们的第一个 go-to 方法将使用大括号，并将其分配给一个变量。但这不是一个空白对象，因为它仍然具有 JavaScript 的对象属性，如 **__proto__** 和其他方法。有一种方法可以创建一个没有任何对象属性的对象。为此，我们使用一个字典，并将其赋给一个空值，其**_ _ 原型 __** 未定义。

*   **代码:**

## java 描述语言

```
<script>

    /* Using .create() method to create
       a completely empty object */

    let dict = Object.create(null);

    // dict.__proto__ === "undefined"
</script>
```

**7。截断数组:**虽然[T3。拼接](https://www.geeksforgeeks.org/javascript-array-splice-method/) **()** 方法被广泛用于切割或移除阵列的特定部分，但它具有 O(n)的最坏情况时间复杂度。对于从数组末尾移除元素，有一个更好的替代方法。它使用**。** [**长度**](https://www.geeksforgeeks.org/javascript-string-length/) 属性的数组这样做。

*   **代码:**

## java 描述语言

```
<script>
let arrayToTruncate = [10, 5, 7, 8, 3, 4, 6, 1, 0];

/* Specifying the length till where the
   array should be truncated */
arrayToTruncate.length = 6; 
console.log(arrayToTruncate)
</script>
```

*   **输出:**如所见，我们必须知道要以这种方式截断的数组长度，否则会导致错误。这里的运行时间是 O(k)，其中 k 是数组中剩余的元素数。

```
[10, 5, 7, 8, 3, 4]
```

**8。合并对象:**扩展操作符(**……**)的引入允许用户容易地合并到一个或多个对象，这是通过创建单独的函数来实现的。

*   **代码 1:**

## java 描述语言

```
<script>
function mergeObjects(obj1, obj2) {
    for (var key in obj2) {
        if (obj2.hasOwnProperty(key)) obj1[key] = obj2[key];
    }
    return obj1;
}
</script>
```

*   **代码 2:** 通过使用 spread 运算符，可以轻松完成上述任务，代码也相当清晰。

## java 描述语言

```
<script>
    const obj1 = {}; // Items inside the object
    const obj2 = {}; // Items inside the object

    const obj3 = {...obj1, ...obj2};
</script>
```

```
Input: 
obj1 = { site:'GeeksforGeeks', purpose:'Education'}
obj2 = { location:'Noida'}

Output:
obj3 = {site:'GeeksforGeeks', purpose:'Education', location:'Noida'}
```

**9。更快的条件检查:**检查和循环条件是每种编程语言必不可少的一部分。在 JavaScript 中，我们是这样做的:

*   **代码 1:**

## java 描述语言

```
<script>
if (condition) {
    doSomething();
}
</script>
```

*   **代码 2:** 然而，位操作符的使用使得检查条件变得更加容易，也使得代码变成一行:

## java 描述语言

```
<script>
    condition && doSomething();
</script>
```

**10。使用正则表达式替换所有字符:**经常会出现这样的情况:一个字符或子字符串的每一次出现，但不幸的是， [**。replace()**](https://www.geeksforgeeks.org/javascript-string-replace/) 方法只替换一个出现的实例。我们可以通过使用带有 [**的正则表达式来解决这个问题。替换()**](https://www.geeksforgeeks.org/javascript-string-replace/) 的方法。

*   **代码:**

## java 描述语言

```
<script>
    var string = "GeeksforGeeks"; // Some string

    console.log(string.replace(/eek/, "ool"));
</script>
```

*   **输出:**

```
"GoolsforGools"
```