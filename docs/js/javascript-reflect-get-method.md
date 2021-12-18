# JavaScript | Reflect.get()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-get-method/](https://www.geeksforgeeks.org/javascript-reflect-get-method/)

JavaScript 中的 **Reflect.get()** 方法用于允许用户从对象中获取属性作为函数。此方法始终返回属性值。
**语法:**

```
Reflect.get(target, propertyKey, receiver) 
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**此参数用于获取属性，是目标对象。
*   **propertyKey:** 此参数用于获取密钥的名称。
*   **receiver:** 它是一个可选参数，如果遇到 getter，它是为对象调用提供的参数值。

**返回值:**这个方法总是返回属性的值。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.get()方法:
**示例 1:**

## java 描述语言

```
const object = {
  val1: 1,
  val2: 2
};
console.log(Reflect.get(object, 'val1'));

const abc = {val:21}; 
console.log( Reflect.get ( abc, "val" ) === 21 ); 
console.log( Reflect.get ( abc, "x" ) === undefined );  
console.log( Reflect.get ( abc, "y" ) === 21 ); 

const array1 = ['geeks1', 'geeks2', 'geeks3', 'geeks4'];
console.log(Reflect.get(array1, 3));
```

**输出:**

```
1
true
true
false
"geeks4"
```

**例 2:**

## java 描述语言

```
let abc = {val: 1};

let obj1 = new Proxy(abc, {
  get(t, k, r) {
    return k + 'for'+ k
  }
})
console.log (Reflect.get(obj1, 'geeks'));

const valx = {prop:21}; 
const valy = Object.create (valx); 
console.log ( 
    Reflect.get ( valy, "prop" ) === 12 
);
console.log ( 
    Reflect.get ( valy, "prop" ) === 21 
);
```

**输出:**

```
"geeksforgeeks"
false
true
```

**支持的浏览器:**JavaScript reflect . get()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上