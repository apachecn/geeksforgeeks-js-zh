# 下划线. js _。合并()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-merge-method/](https://www.geeksforgeeks.org/underscore-js-_-merge-method/)

**_。merge()方法** m 从最左边到最右边合并两个或多个对象，以创建父映射对象。

**语法:**

```
_.merge(obj1, obj2,..., objn);

```

**参数:**该方法取 **n 个对象**进行合并。

**返回值:**这个方法返回一个新生成的合并对象。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = _.merge({ a: "1" }, { b: "2" }, { c:"3" });;

console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Generated Mapping Object:  { a: '1', b: '2', c: '3' }

```

**示例 2:** 如果两个键相同，则生成的对象将具有最右边键的值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = _.merge({ a: "1" }, { a: "2" }, 
                  { b: "2" }, { c:"3" });;

console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Generated Mapping Object:  { a: '2', b: '2', c: '3' }

```

**示例 3:** 如果多个对象相同，新生成的对象将只有一个键和值对应于这些对象。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = _.merge({ a: "1" }, { a: "1" }, 
                  { b: "2" }, { c:"3" });;

console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Generated Mapping Object:  { a: '1', b: '2', c: '3' }

```

**例 4:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var obj = _.merge({ a: "1",  d: "4"}, 
                  { a: "1" }, { b: "2" }, 
                  { c:"3" });;

console.log("Generated Mapping Object: ", obj);
```

**输出:**

```
Generated Mapping Object:  { a: '1', d: '4', b: '2', c: '3' }

```