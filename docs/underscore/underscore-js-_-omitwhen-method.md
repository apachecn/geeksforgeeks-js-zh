# 下划线. js _。omitWhen()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-omitwhen-method/](https://www.geeksforgeeks.org/underscore-js-_-omitwhen-method/)

**_。omitWhen()** 方法返回对象的副本，省略给定谓词函数返回真的那些属性。谓词函数用每个属性值调用。

**语法:**

```
_.omitWhen( Object_name, predicate_func );
```

**参数:**

*   **对象名称:**要省略键/值对的对象。
*   **谓词 _ 函数:**包含属性条件的给定函数将被省略

**返回值:**此方法 r 在省略属性后返回对象的副本。

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

var val=_.omitWhen(obj, function (id) 
         { return id == "Gfg2" });
console.log(val);
```

**输出:**

```
{ '1': 'Gfg1', '3': 'Gfg3' }
```

**例 2: I** 如果在对象中没有找到属性，这个方法什么都不省略。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = {
    1: "Gfg1",
    2: "Gfg2",
    3: "Gfg3"
};

var val=_.omitWhen(obj, function (id) 
          { return id == "Gfg4" });
console.log(val);
```

**输出:**

```
{ '1': 'Gfg1', '2': 'Gfg2', '3': 'Gfg3' }
```