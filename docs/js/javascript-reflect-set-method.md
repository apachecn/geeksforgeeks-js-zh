# JavaScript | Reflect.set()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-set-method/](https://www.geeksforgeeks.org/javascript-reflect-set-method/)

JavaScript 中的 **Reflect.set()** 方法用于设置对象属性的值。
**语法:**

```
Reflect.set(obj, Key, value, receiver) 
```

**参数:**该方法接受上述四个参数，描述如下:

*   **Obj:** 此参数保存目标对象，用于设置属性。
*   **键:**此参数保存要设置的属性的名称。
*   **值:**该参数保存要设置的值。
*   **Receiver:** 这是一个可选参数，如果遇到 setter，将为对目标的调用提供该参数的值。

**返回值:**该方法返回一个布尔值，该值指示属性是否设置成功。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.set()方法:
**示例 1:**

## java 描述语言

```
const object1 = {};
Reflect.set(object1, 'property1', "NULL");
console.log(object1.property1);

const array1 = ['geeks', 'valt', 'geeks'];
Reflect.set(array1, 2, 'for');
console.log(array1[2]);

const val1={}; 
const val2={}; 
Reflect.set(val1, 'prop1', 45); 
console.log(val1.prop1); 
Reflect.set(val2, 'prop2', 567); 
console.log(val2.prop2);
```

**输出:**

```
"NULL"
"for"
45
567
```

**例 2:**

## java 描述语言

```
let obj1 = {}
console.log(Reflect.set(obj1, 'prop', 'value') );
console.log(obj1.prop );

// Initializing an array
let arr = ['geek1', 'geek2', 'geek3']
console.log(Reflect.set(arr, 2, 'geek4') );
console.log(arr[2]);

// It can truncate an array.
console.log(Reflect.set(arr, 'length', 1)  );
console.log(arr);

// With just one argument, propertyKey
// and value are "undefined".
let obj = {}
console.log(Reflect.set(obj)  );
console.log(Reflect.getOwnPropertyDescriptor(
                 obj, 'undefined')); 
```

**输出:**

```
true
"value"
true
"geek4"
true
Array ["geek1"]
true
Object { value: undefined, writable: true, enumerable: true, configurable: true }
```

**支持的浏览器:**JavaScript reflect . set()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上