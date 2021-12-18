# 洛达什 _。克隆()方法和“=”操作符来复制对象

> 原文:[https://www . geesforgeks . org/difference-lodash-_-克隆方法和操作符到复制对象/](https://www.geeksforgeeks.org/difference-between-lodash-_-clone-method-and-operator-to-copy-objects/)

在本文中，我们将了解使用 _。clone()方法，并使用“=”运算符复制对象。这两种方法都用于在 JavaScript 中创建对象的副本。然而，两者的工作方式截然不同。

**使用 _。克隆()方法:****_。clone()方法**创建一个新对象，并将每个值从原始对象复制到新对象。这将创建一个对象的浅拷贝。对原始对象的任何更改都不会影响复制的对象。

**语法:**

```
_.clone( object )
```

**参数:**该函数只接受一个参数，即需要复制的对象。

**返回值:**返回给定对象的浅拷贝。

**示例:**下面的示例显示，更改原始对象不会影响使用 _ 复制的对象。clone()函数。

## java 描述语言

```
const _ = require("lodash");

var originalflower = {
    Name: "Rose",
    color: "Red",
    petal: 5,
};

// Creating a copy of the object
var copyflower = _.clone(originalflower);

// Printing the cloned object
console.log("Cloned object : ",
        copyflower);

// As this is a shallow copy, changing
// attributes of one object will not
// affect other object
originalflower.Name = "Red Rose";

// Printing original flower
// and cloned flower
console.log("original flower: ",
        originalflower);

console.log("copy flower: ", copyflower);
```

**输出:**

```
Cloned object :  { Name: 'Rose', color: 'Red', petal: 5 }
original flower:  { Name: 'Red Rose', color: 'Red', petal: 5 }
copy flower:  { Name: 'Rose', color: 'Red', petal: 5 }
```

**使用“=”运算符复制对象:**在这种方法中，只需使用“=”运算符即可将复制的对象指向已经存在的原始对象。原始对象的更改确实会影响复制的对象。

**示例:**以下示例显示，更改原始对象会影响使用“=”运算符复制的对象。

## java 描述语言

```
const _ = require("lodash");

var originalFlower = {
    Name: "Rose",
    color: "Red",
    petal: 5,
};

// Creating a copy of originalFlower
var copyFlower = originalFlower;
console.log("Copy object : ",
    copyFlower);

// As both originalFlower and
// copyFlower point to same object
// Changing one object will
// affect other also
originalFlower.Name = "Red Rose";

// Printing the Name attribute
// of originalFlower and copyFlower.
console.log("The name of original flower is - ",
    originalFlower.Name);
console.log("The name of copy flower is - ",
    copyFlower.Name);
```

**输出:**

```
Copy object :  { Name: 'Rose', color: 'Red', petal: 5 }
The name of original flower is -  Red Rose
The name of copy flower is -  Red Rose
```