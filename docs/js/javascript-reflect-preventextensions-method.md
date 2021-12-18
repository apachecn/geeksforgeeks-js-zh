# JavaScript | reflect . preventexturements()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-reflect-preventextensions-method/](https://www.geeksforgeeks.org/javascript-reflect-preventextensions-method/)

Javascript 中的**reflect . preventextenvironments()**方法用于防止对象的未来扩展，这意味着防止向对象添加新属性。
**语法:**

```
Reflect.preventExtensions( obj )  
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Obj:** 此参数保存目标对象，用于防止扩展。

**返回值:**该方法返回布尔值。对于成功防止扩展，它返回真。否则，返回 false。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
下面的示例说明了 JavaScript 中的**reflect . preventextenvironments()方法:**
**示例 1:**

## java 描述语言

```
const object1 = {};

console.log(Reflect.isExtensible(object1));
Reflect.preventExtensions(object1);
console.log(Reflect.isExtensible(object1));

const obj = {}; 
Reflect.preventExtensions(obj); 
console.log( 
Reflect.isExtensible(obj) 
);   
obj.val = 3; 
console.log( 
    obj.hasOwnProperty ("val") 
); 
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
let empty = {}
console.log(Reflect.isExtensible(empty));
console.log(Reflect.preventExtensions(empty));
console.log(Reflect.isExtensible(empty));

const obj = {"val1":3, "val2":4}; 
Reflect.preventExtensions(obj); 
console.log ( obj.hasOwnProperty ( "val1" ) );  
delete obj.val1; 
console.log ( obj.hasOwnProperty ( "val2" ) ); 
```

**输出:**

```
true
true
false
true
true
```

**支持的浏览器:**下面列出了**reflect . preventextessions()方法**支持的浏览器:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上