# JavaScript | reflect . deleteproperty()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-delete property-method/](https://www.geeksforgeeks.org/javascript-reflect-deleteproperty-method/)

JavaScript 中的 **Reflect.deleteProperty()方法**用于删除对象上的属性。它返回一个布尔值，该值指示属性是否被成功删除。
**语法:**

```
Reflect.deleteProperty( target, propertyKey )
```

**参数:**该方法接受两个参数，如下文所述:

*   **目标:**此参数删除属性，是目标对象。
*   **propertyKey:** 此参数是要删除的属性的名称。

**返回值:**该方法返回一个布尔值，该值指示属性是否被成功删除。
**异常:**当目标不是构造函数时，类型错误是作为结果给出的异常。
**例 1:**

## java 描述语言

```
const object1 = {
  property1: 76
};

Reflect.deleteProperty(object1, 'property1');

console.log(object1.property1);

const array1 = [1, 2, 3, 4, 5];
Reflect.deleteProperty(array1, '12');
console.log(array1);

Reflect.deleteProperty(array1, '1');
console.log(array1);

Reflect.deleteProperty(array1, '2');
console.log(array1);
```

**输出:**

```
undefined
Array [1, 2, 3, 4, 5]
Array [1, undefined, 3, 4, 5]
Array [1, undefined, undefined, 4, 5]
```

**例 2:**

## java 描述语言

```
// Returns true if no such property exists
document.writeln( Reflect.deleteProperty({}, 'geeks'))

// Returns false if a property is unconfigurable
document.writeln( Reflect.deleteProperty(
       Object.freeze({geeks: 1}), 'geeks'))

const obj = {val1: 22, val2:434, val3:42}; 
const obj1 = {val:5};
document.writeln( Reflect.deleteProperty ( obj, "val1" ) ); 
document.writeln( Reflect.deleteProperty ( obj, "val2" ) );  
```

**输出:**

```
true false true true
```

**支持的浏览器:****reflect . deleteproperty()方法**支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safar 10 及以上