# 下划线. js _。pickWhen()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-pickwhen-method/](https://www.geeksforgeeks.org/underscore-js-_-pickwhen-method/)

**_。pickWhen()** 方法返回对象的副本，该对象包含给定谓词函数返回 true 的那些属性。谓词函数用每个属性值调用。

**语法:**

```
_.pickWhen( Object_name, predicate_func );
```

**参数:**

*   **对象名称:**从中选取键/值对的对象。
*   **谓词 _ 函数:**包含属性条件的给定函数将被选取

**返回值:**此方法 r 在包含属性后返回一个对象的副本。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = {
    1: "Gfg1",
    2: "Gfg2",
    3: "Gfg3"
};

var val = _.pickWhen(obj, function (id) 
          { return id == "Gfg1" });
console.log(val);
```

**输出:**

```
{ '1': 'Gfg1' }
```

**例 2:如果在对象中没有找到属性，这个方法什么都不选。**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = {
    1: "Gfg1",
    2: "Gfg2",
    3: "Gfg3"
};

var val = _.pickWhen(obj, function (id) 
          { return id == "Gfg4" });
console.log(val);
```

**输出:**

```
{}
```