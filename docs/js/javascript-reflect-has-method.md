# JavaScript | Reflect.has()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-has-method/](https://www.geeksforgeeks.org/javascript-reflect-has-method/)

JavaScript 中的 **Reflect.has()** 方法用于检查对象中是否存在该属性。它的工作原理类似于函数中的运算符。
**语法:**

```
Reflect.has(target, propertyKey) 
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **目标:**这个参数是目标对象，它寻找属性。
*   **propertyKey:** 此参数是要检查的属性的名称。

**返回值:**该方法返回一个布尔值，该值指示目标是否具有该属性。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.has()方法:
**示例 1:**

## java 描述语言

```
<script>
const object1 = {
    property1: 434
};

console.log(Reflect.has(object1, 'property1'));
console.log(Reflect.has(object1, 'property2'));
console.log(Reflect.has(object1, 'toString'));

var x = { foo: 1 };
console.log(Reflect.has(x, 'foo'));
console.log('foo' in x);
console.log(Reflect.has(x, 'bar'));
console.log('bar' in x);
</script>
```

**输出:**

```
true
false
true
true
true
false
false
```

**例 2:**

## java 描述语言

```
<script>

// Returns true for properties in
// the prototype chain
console.log(Reflect.has({x: 0}, 'toString') );

// Proxy with .has() handler method
let obj = new Proxy({}, {
    has(t, k) { return k.startsWith('geeks')  }
});
console.log(Reflect.has(obj, 'geeksforgeeks'));
console.log(Reflect.has(obj, 'geekforgeek'));

const val1 = {foo: 123}
const val2 = {__proto__: val1}
const val3 = {__proto__: val2}

// The prototype chain is: c -> b -> a
console.log(Reflect.has(val3, 'foo'));
</script>
```

**输出:**

```
true
true
false
true
```

**支持的浏览器:**JavaScript reflect . has()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上