# JavaScript object . preventexturements()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-preventextivens-method/](https://www.geeksforgeeks.org/javascript-object-preventextensions-method/)

JavaScript 中的**object . PrevenTextExtensions()方法**是标准的内置对象，可防止新属性被添加到对象中。
**语法:**

```
Object.preventExtensions( obj )
```

**参数:**该方法接受上述单个参数，描述如下:

*   **obj:** 该参数保存必须不可扩展的对象。

**返回值:**该方法在使对象不可扩展后返回对象。
以下示例说明了 JavaScript 中的 Object.preventExtensions()方法:
**示例 1:**

## java 描述语言

```
let geeks1 = {};

Object.preventExtensions(geeks1);

try {
  Object.defineProperty(geeks1, 'prop1', {
    value: "GFG",
    property1:"Geeksforgeeks",
    property2:"Best platform to learn"
  });
} catch (error) {
  console.log(error);
}
```

**输出:**

```
TypeError: Cannot define property prop1, object is not extensible
```

**例 2:**

## java 描述语言

```
var geeks = {};
var geeks0 = Object.preventExtensions(geeks);
console.log( geeks0 === geeks);

const geeks1 = {"prop1": 555}; 
Object.preventExtensions(geeks1); 
delete geeks1.prop1; 
console.log ( geeks1.hasOwnProperty ( "prop1" ) );

const geeks2 = {}; 
Object.preventExtensions(geeks2); 
geeks2.prop2 = 3; 

console.log( 
    geeks2.hasOwnProperty("prop2") 
);  

const geeks3 = {}; 
Object.preventExtensions(geeks3); 
console.log( 
    Object.isExtensible(geeks3) 
);
```

**输出:**

```
true
false
false
false
```

**支持的浏览器:**object . preventextionss()方法支持的浏览器如下:

*   Chrome 6 及以上
*   边缘 12 及以上
*   Firefox 4 及以上版本
*   Internet Explorer 9 及以上版本
*   歌剧 12 及以上
*   safari 5.1 及以上版本