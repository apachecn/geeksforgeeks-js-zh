# 什么是 JavaScript 中的对象相等？

> 原文:[https://www . geeksforgeeks . org/什么是对象平等 javascript/](https://www.geeksforgeeks.org/what-is-object-equality-in-javascript/)

JavaScript 为我们提供了许多检查两个对象是否相等的方法。让我们演示如何检查两个对象是否相等。

有三种类型的平等

*   参照平等。
*   肤浅的平等。
*   完全平等。

**引用相等:**我们可以说，当两个对象的指针相同时，或者当操作符是同一对象实例时，两个对象是引用相等的。

我们可以用三种方法检查引用相等性:

*   ===(三重相等)运算符或严格相等运算符。严格意义上的平等是指两种价值观的平等。如果两个值具有相同的类型，则认为它们相等。
*   == (double equals)是松散相等运算符。它将这两个值转换为一个公共类型，然后检查是否相等。
*   [**【对象】()**](https://www.geeksforgeeks.org/object-is-in-javascript/) 功能。

[**==操作员:**](https://www.geeksforgeeks.org/javascript-operators/)

## java 描述语言

```
<script>
    var a = 1;
    var b = 1;
    console.log(a == b); // true
    var c = 10;
    var d = "10";
    console.log(c == d); // true

    const name1 = {
        first_name: "sarah",
    };

    const name2 = {
        first_name: "sarah",
    };

    console.log(name1 == name2); // false
</script>
```

**输出:**

```
true
true
false
```

[**===操作员:**](https://www.geeksforgeeks.org/javascript-operators/)

## java 描述语言

```
<script>
    var a = 1;
    var b = 1;

    console.log(a === b); // true
    var c = 10;
    var d = "10";

    console.log(c === d); // false

    const name1 = {
        first_name: "sarah",
    };

    const name2 = {
        first_name: "sarah",
    };

    console.log(name1 === name2); // false
</script>
```

**输出:**

```
true
false
false
```

[**object.is()方法:**](https://www.geeksforgeeks.org/object-is-in-javascript/)

## java 描述语言

```
<script>
    var a = 1;
    var b = 1;

    var c = 10;
    var d = "10";

    console.log(Object.is(c, d)); // false
    console.log(Object.is(a, b)); // true
    console.log(Object.is(a, a)); // true

    const name1 = {
        first_name: "sarah",
    };

    const name2 = {
        first_name: "sarah",
    };

    console.log(Object.is(name1, name2)); // false
    console.log(Object.is(name1, name1)); // true
</script>
```

**输出:**

```
false
true
true
false
true
```

**浅相等:**

*   对象的浅层相等检查返回两个对象的属性列表，并进一步检查属性是否相等。
*   浅层相等是当两个对象中的键值相等时发生的一种相等。

**深度相等:**

*   深度相等是递归的浅相等检查。
*   如果属性是对象，则递归地对这些对象执行检查。