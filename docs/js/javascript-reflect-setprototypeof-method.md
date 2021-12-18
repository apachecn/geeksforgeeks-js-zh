# JavaScript | reflect . set rototypeof()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-set rototypeof-method/](https://www.geeksforgeeks.org/javascript-reflect-setprototypeof-method/)

JavaScript 中的**reflect . set rototypeof()**方法用于将指定对象的原型设置为另一个对象或 Null。此方法为成功的操作返回布尔值。
**语法:**

```
Reflect.setPrototypeOf(obj, prototype)
```

**参数:**

*   **Obj:** 此参数保存目标对象，用于设置原型。
*   **原型:**此参数保存对象的新原型。它可以是任何对象，也可以只是一个空值。

**返回值:**该方法总是返回一个布尔值，该值指示原型设置是否成功完成。
**异常:**当目标不是对象时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.setPrototypeOf()方法:
**示例 1:**

## java 描述语言

```
const object1 = {};

console.log(Reflect.setPrototypeOf(object1, Object.prototype));
console.log(Reflect.setPrototypeOf(object1, null));

const object2 = {};
console.log(Reflect.setPrototypeOf(Object.freeze(object2), null));

let object3 = { 
  gfg() { 
    return 'value'; 
  } 
} 
let obj = { 
  geeks() { 
    return 'answer'; 
  } 
} 
Object.setPrototypeOf(obj, object3); 
console.dir(obj);  
console.log(obj.geeks());   
console.log(obj.gfg()); 
```

**输出:**

```
true
true
false
"answer"
"value"
```

**例 2:**

## java 描述语言

```
console.log(Reflect.setPrototypeOf({}, Object.prototype) );

// It can change an object's [[Prototype]] to null.
console.log(Reflect.setPrototypeOf({}, null));

// Returns false if target is not extensible.
console.log(Reflect.setPrototypeOf(Object.freeze({}), null)); 

// Returns false if it cause a prototype chain cycle.
let target = {}
let proto = Object.create(target)
console.log(Reflect.setPrototypeOf(target, proto) ); 

var object3 = { 
   gfg() { 
     console.log(this.name + ' have fun.'); 
   } 
}; 
class objt { 
   constructor(name) { 
   this.name = name; 
  } 
} 
Reflect.setPrototypeOf(objt.prototype, object3); 

// If you do not do this you will get
// a TypeError when you invoke speak 
var val = new objt('Geeks'); 
val.gfg();
```

**输出:**

```
true
true
false
false
"Geeks have fun."
```

**支持的浏览器:**JavaScript reflect . set rototypeof()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上