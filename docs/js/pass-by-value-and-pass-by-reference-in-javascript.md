# 在 Javascript 中按值传递和按引用传递

> 原文:[https://www . geesforgeks . org/按值传递和按引用传递 javascript/](https://www.geeksforgeeks.org/pass-by-value-and-pass-by-reference-in-javascript/)

在本文中，我们将讨论 JavaScript 中的按值传递和按引用传递。

**按值传递:**在按值传递中，通过直接传递变量的值作为参数来调用函数。因此，函数内部的任何更改都不会影响原始值。

在按值传递中，作为参数传递的参数创建其自己的**副本。**所以在函数内部所做的任何更改都是针对复制的值，而不是原始值。

让我们举个例子来更好地理解:

## java 描述语言

```
function Passbyvalue(a, b) {
    let tmp;
    tmp = b;
    b = a;
    a = tmp;
    console.log(`Inside Pass by value 
        function -> a = ${a} b = ${b}`);
}

let a = 1;
let b = 2;
console.log(`Before calling Pass by value 
        Function -> a = ${a} b = ${b}`);

Passbyvalue(a, b);

console.log(`After calling Pass by value 
       Function -> a =${a} b = ${b}`);
```

**输出:**

```
Before calling Pass by value Function -> a = 1 b = 2
Inside Pass by value function -> a = 2 b = 1
After calling Pass by value Function -> a =1 b = 2
```

**通过引用传递:**在通过引用传递中，通过直接传递变量的引用/地址作为参数来调用函数。所以改变函数内部的值也会改变原来的值。在 JavaScript 中**数组和对象**遵循按引用传递属性。

在“按引用传递”中，作为参数传递的参数不会创建自己的副本，而是引用原始值，因此在函数内部进行的更改会影响原始值。

让我们举个例子来更好地理解。

## java 描述语言

```
function PassbyReference(obj) {
    let tmp = obj.a;
    obj.a = obj.b;
    obj.b = tmp;

    console.log(`Inside Pass By Reference 
        Function -> a = ${obj.a} b = ${obj.b}`);
}

let obj = {
    a: 10,
    b: 20

}
console.log(`Before calling Pass By Reference 
    Function -> a = ${obj.a} b = ${obj.b}`);

PassbyReference(obj)

console.log(`After calling Pass By Reference 
    Function -> a = ${obj.a} b = ${obj.b}`);
```

**输出:**

```
Before calling Pass By Reference Function -> a = 10 b = 20
Inside Pass By Reference Function -> a = 20 b = 10
After calling Pass By Reference Function -> a = 20 b = 10
```

**注意:**在通过引用中，我们正在对原始值进行变异。当我们传递一个对象作为参数，并在函数的上下文中更新该对象的引用时，这不会影响对象的值。但是如果我们在内部变异这个对象，它会影响这个对象。

**示例 1:** 更新函数中的对象引用。

## java 描述语言

```
function PassbyReference(obj) {

    // Changing the reference of the object
    obj = {
        a: 10,
        b: 20,
        c: "GEEKSFORGEEKS"
    }
    console.log(`Inside Pass by 
        Reference Function -> obj `);

    console.log(obj);
}

let obj = {
    a: 10,
    b: 20

}
console.log(`Updating the object reference -> `)
console.log(`Before calling Pass By 
        Reference Function -> obj`);
console.log(obj);

PassbyReference(obj)
console.log(`After calling Pass By 
        Reference Function -> obj`);
console.log(obj);
```

**输出:**

```
Updating the object reference -> 
Before calling PassByReference Function -> obj
{a: 10, b: 20}
Inside PassbyReference Function -> obj 
{a: 10, b: 20, c: "GEEKSFORGEEKS"}
After calling PassByReference Function -> obj
{a: 10, b: 20}
```

**示例 2:** 对原始对象进行突变。

## java 描述语言

```
function PassbyReference(obj) {

    // Mutating the origanal object 
    obj.c = "GEEKSFORGEEKS";
    console.log(`Inside Pass by
        Reference Function -> obj `);
    console.log(obj);
}

let obj = {
    a: 10,
    b: 20

}
console.log(`Mutating the origanal object -> `)
console.log(`Before calling Pass By
        Reference Function -> obj`);
console.log(obj);

PassbyReference(obj)
console.log(`After calling Pass By 
        Reference Function -> obj`);
console.log(obj);
```

**输出:**

```
Mutating the origanal object -> 
Before calling PassByReference Function -> obj
{a: 10, b: 20}
Inside PassbyReference Function -> obj 
{a: 10, b: 20, c: "GEEKSFORGEEKS"}
After calling PassByReference Function -> obj
{a: 10, b: 20, c: "GEEKSFORGEEKS"}
```