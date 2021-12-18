# JavaScript | reflect . isextensable()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-isextensible-method/](https://www.geeksforgeeks.org/javascript-reflect-isextensible-method/)

JavaScript 中的**reflect . iseextensible()方法**用于检查对象是否可扩展。此方法类似于 Object.isExtensible()，但如果目标不是对象，它将导致类型错误。
**语法:**

```
Reflect.isExtensible( obj )
```

**参数:**该方法接受上述单个参数，描述如下:

*   **Obj:** 此参数为目标对象，用于检查是否可扩展。

**返回值:**该方法返回一个布尔值，该值指示目标是否可扩展。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.isExtensible()方法:
**示例 1:**

## java 描述语言

```
<script>
const object1 = {};

console.log(Reflect.isExtensible(object1));
Reflect.preventExtensions(object1); 
console.log(Reflect.isExtensible(object1));

const object2 = Object.seal({}); 
console.log(Reflect.isExtensible(object2)); 

const object3 = Object.seal({}); 
console.log(Reflect.isExtensible(object3));
</script>
```

**输出:**

```
true
false
false
false
```

**例 2:**

## java 描述语言

```
<script>

// Sealed objects are by definition
// non-extensible.
let sealed = Object.seal({}) 
console.log(Reflect.isExtensible(sealed));

let empty = {}
console.log(Reflect.isExtensible(empty));

// ...but that can be changed.
Reflect.preventExtensions(empty) 
console.log(Reflect.isExtensible(empty));

// Frozen objects are also by
// definition non-extensible.
let frozen = Object.freeze({}) 
console.log(Reflect.isExtensible(frozen));
</script>
```

**输出:**

```
false
true
false
false
```

**支持的浏览器:**JavaScript reflect . construct()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上