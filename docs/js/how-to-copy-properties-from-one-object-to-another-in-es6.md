# 如何在 ES6 中将属性从一个对象复制到另一个对象？

> 原文:[https://www . geesforgeks . org/如何在 es6 中将属性从一个对象复制到另一个对象/](https://www.geeksforgeeks.org/how-to-copy-properties-from-one-object-to-another-in-es6/)

一个对象的属性可以通过不同的方法复制到另一个对象中。以下是其中一些方法。

[**Object.assign()**](https://www.geeksforgeeks.org/object-assign-javascript/)**:**通过使用 object . assign()方法，一个或多个源对象的所有可枚举属性都被复制到目标对象。此方法返回修改后的目标对象。如果目标对象的属性与源中的属性具有相同的键，则目标对象的属性将被覆盖。来自较新来源的属性会覆盖来自较早来源的属性。Object.assign()只将可枚举和自己的属性从一个对象复制到另一个对象。因此，它在源和目标上调用 getters 和 setters。因此，它分配属性而不是复制或定义新的属性。合并源可能包含 getters，因此不适合将新属性合并到原型中。

**语法:**

```
Object.assign(target, ...sources)
```

**示例:**

## Java Script 语言

```
<script>
    let obj1 = { a: 1, b: 2 };
    let obj2 = { a: 3, c: 4 };
    let obj3 = { b: 5, d: 6 };

    // Target object itself is changed.
    let targetobj1 = Object.assign(obj1, obj2);

    // Here the obj1 and targetobj1 both are same
    console.log(obj1);
    console.log(targetobj1);

    // Passing multiple objects and copy
    // to the target obj
    let targetobj2 = Object.assign(obj1, obj2, obj3);
    console.log(obj1);
    console.log(targetobj2);
</script>
```

**输出:**

```
{
    a: 3,
    b: 2,
    c: 4
}
{
    a: 3,
    b: 2,
    c: 4
}
{
    a: 3,
    b: 5,
    c: 4,
    d: 6
}
{
    a: 3,
    b: 5,
    c: 4,
    d: 6
}
```

**使用** [**扩展运算符**](https://www.geeksforgeeks.org/javascript-spread-operator/) **:** 数组表达式或字符串可以使用扩展语法(…)在没有或有多个参数(用于函数调用)或元素(用于数组文字)的地方进行扩展，或者对象表达式可以在没有或有多个键值对(用于对象文字)的地方进行扩展。

## Java Script 语言

```
<script>
    let obj1 = { a: 1, b: 2 };
    let obj2 = { a: 3, c: 4 };
    let obj3 = { b: 5, d: 6 };

    // (...) is syntax of spread operator
    let targetobj = { ...obj1, ...obj2, ...obj3 };
    console.log(targetobj);
</script>

```

**输出:**

```
{
    a: 3,
    b: 5,
    c: 4,
    d: 6
}
```

**通过使用 for 循环:**需要迭代源对象(即 obj2)的属性，并将带有值的属性赋给目标对象 obj1。但是，如果我们使用一个对象进行循环，则该方法仅限于两个对象。

## Java Script 语言

```
<script>
    let obj1 = { a: 1, b: 2 };
    let obj2 = { a: 3, c: 4 };
    for (let key in obj2) {
        obj1[key] = obj2[key];
    }
    console.log(obj1);
</script>
```

**输出:**

```
{
    a: 3,
    b: 2,
    c: 4
}
```