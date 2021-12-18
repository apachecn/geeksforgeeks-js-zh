# JavaScript object . prototype . properties isenumerable()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-prototype-properties isenumerable-method/](https://www.geeksforgeeks.org/javascript-object-prototype-propertyisenumerable-method/)

方法**properties isenumerable()**返回一个布尔值，指示指定的属性是否可枚举，是否是对象自己的属性。如果对象没有指定的属性，此方法返回 false。

**语法:**

```
obj.propertyIsEnumerable(prop)
```

*   **Prop:** The name of the property to be tested.

**返回值:**布尔值。

**例 1:**

## java 描述语言

```
const obj = {};
const arr = [];
obj.property = 42;
arr[0] = 42;

console.log(obj.propertyIsEnumerable('property'));
console.log(arr.propertyIsEnumerable(0));
console.log(arr.propertyIsEnumerable('length'));
```

**输出:**

```
true
true
false
```

**示例 2:** 以下示例说明了用户定义属性与内置属性的可枚举性:

## JavaScript

```
let a = ['is enumerable'];

console.log(a.propertyIsEnumerable(0));        
console.log(a.propertyIsEnumerable('length'));  

console.log(Math.propertyIsEnumerable('random')); 
console.log(this.propertyIsEnumerable('Math'));    
```

**输出:**

```
true
false
false
false
```

**支持的浏览器:**

*   Chrome 1 and above
*   Edge 12 and above
*   Firefox 1 and above
*   微软公司出品的 web 浏览器
*   Opera 4 and above
*   Safari 3 and above