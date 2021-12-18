# JavaScript | object . getowntpropertysdescriptor()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-getownpertysdescriptor-method/](https://www.geeksforgeeks.org/javascript-object-getownpropertydescriptor-method/)

JavaScript 中的**object . getowntpropertysdescriptor()方法**是标准的内置对象，它返回给定对象自身属性的属性描述符。
**语法:**

```
Object.getOwnPropertyDescriptor( obj, prop )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **obj:** 此参数保存要查看属性的对象。
*   **道具:**此参数保存要检索其描述的属性的名称或符号。

**返回值:**该方法根据对象的存在，返回给定属性或未定义属性的属性描述符。
以下示例说明了 JavaScript 中的 object . getowntpropertysdescriptor()方法:
**示例 1:**

## java 描述语言

```
const geeks1 = { 
  prop1: "GeeksforGeeks" 
} 
const geeks2 = { 
  prop2: "Best Platform" 
} 
const geeks3 = { 
  prop3: "And Computer science portal" 
}
const descriptor1 = Object.getOwnPropertyDescriptor(geeks1, 'prop1'); 
const descriptor2 = Object.getOwnPropertyDescriptor(geeks2, 'prop2'); 
const descriptor3 = Object.getOwnPropertyDescriptor(geeks3, 'prop3'); 
console.log(descriptor1.enumerable); 
console.log(descriptor2.enumerable); 
console.log(descriptor1.value); 
console.log(descriptor2.value); 
console.log(descriptor3.enumerable); 
console.log(descriptor3.value); 
```

**输出:**

```
true
true
"GeeksforGeeks"
"Best Platform"
true
"And Computer science portal"
```

**例 2:**

## java 描述语言

```
var geek, result;
geek = { get foo() { return 17; } };
d = Object.getOwnPropertyDescriptor(geek, 'foo');
console.log(d)

geek = { bar: 42 };
d = Object.getOwnPropertyDescriptor(geek, 'bar');
console.log(d)

geek = { [Symbol.for('baz')]: 73 }
d = Object.getOwnPropertyDescriptor(geek, Symbol.for('baz'));
console.log(d)

geek = {};
Object.defineProperty(geek, 'qux', {
  value: 8675309,
  writable: false,
  enumerable: false
});
d = Object.getOwnPropertyDescriptor(geek, 'qux');
console.log(d)
```

**输出:**

```
Object { get: get foo() { return 17; }, set: undefined, enumerable: true, configurable: true }
Object { value: 42, writable: true, enumerable: true, configurable: true }
Object { value: 73, writable: true, enumerable: true, configurable: true }
Object { value: 8675309, writable: false, enumerable: false, configurable: false }
```

**支持的浏览器:**object . getowntpropertysdescriptor()方法支持的浏览器如下:

*   谷歌 Chrome 5.0 及以上版本
*   Internet Explorer 9.0 及以上版本
*   Mozilla 4.0 及以上版本
*   歌剧 12 及以上
*   Safari 5.0 及以上版本