# JavaScript | reflect . defineperoperty()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-definepreproperty-method/](https://www.geeksforgeeks.org/javascript-reflect-defineproperty-method/)

JavaScript 中的**reflect . defineperoperty()**方法用于精确添加或修改对象的属性。此方法返回一个布尔值，该值指示属性是否已成功定义。
**语法:**

```
Reflect.defineProperty(target, propertyKey, attributes) 
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**此参数定义属性和目标对象。
*   **属性键:**此参数是要定义或修改的属性的名称。
*   **属性:**该参数是正在定义或修改的属性的属性。

**返回值:**该方法返回一个布尔值，该值指示属性是否定义成功。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.defineProperty()方法:
**示例 1:**

## java 描述语言

```
const object1 = {};

if (Reflect.defineProperty(object1, 'geeks1', {value: 42})) {
  console.log('geeks1 assigned');

} else {
  console.log('problem created by  geeks1');
}

console.log(object1.geeks1);

const object2 = {};
const object3 = {};
(Reflect.defineProperty(object2, 'geeks2', {value: 97})) 
if (Reflect.defineProperty(object3, 'geeks3', {value: 23})) { 
  console.log('geeks3 assigned'); 
} else { 
  console.log('problem created by geeks3'); 
} 
console.log(object3.geeks3); 
console.log(object2.geeks2);
```

**输出:**

```
"geeks1 assigned"
42
"geeks3 assigned"
23
97
```

**例 2:**

## java 描述语言

```
const a = {}; 
const result = Reflect.defineProperty(a, "geek1", 
{ value : 19, }); 

console.log(a);
console.log( result);  

const b = {}; 
const result1 = Reflect.defineProperty(b, "geek2", 
{ value : 56, 
  writable: false
} 
); 
console.log(b ); 
console.log(result1);

let obj = {}
Reflect.defineProperty(obj, 'x', {value: 71})  // true
console.log(obj.x)
```

**输出:**

```
Object {  }
true
Object {  }
true
71
```

**支持的浏览器:**JavaScript reflect . defineperoperty()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上