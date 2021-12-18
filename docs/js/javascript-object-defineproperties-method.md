# JavaScript | object . defineperoperties()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-definepreproperties-method/](https://www.geeksforgeeks.org/javascript-object-defineproperties-method/)

JavaScript 中的**Object . defineperoperties()方法**是一个标准的内置对象，它直接在一个对象上定义一个新的或修改现有的属性，并返回该对象。
**语法:**

```
Object.defineProperties(obj, props) 
```

**参数:**

*   **对象:**该参数保存将要定义或修改属性的对象。
*   **道具:**该参数是一个对象，其自身的可枚举属性构成了待定义或修改属性的描述符。

**返回值:**该方法返回一个对象，该对象作为参数传递给函数。
以下示例说明了 JavaScript 中的 Object.defineProperties()方法:
**示例 1:**

## java 描述语言

```
const geek = {};

Object.defineProperties(geek, {
  prop1: {
    value: "geeksforgeeks",
    writable: true
  },
  prop2: {}
});

console.log(geek.prop1);
console.log(geek.prop2);
```