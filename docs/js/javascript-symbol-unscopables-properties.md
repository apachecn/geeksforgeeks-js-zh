# JavaScript | symbol . unspeciable 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-unscopedables-properties/](https://www.geeksforgeeks.org/javascript-symbol-unscopables-properties/)

Javascript 中的**symbol . unscopedables**属性是一个众所周知的符号，用于指定一个对象值，该对象的自身和继承的属性名称被排除在环境绑定之外。

**语法:**

```
object[Symbol.unscopables]
```

**属性属性:**该属性保存一个对象，它不可写、不可枚举、不可配置。

**返回值:**勾选出现在词法范围变量中的变量。

以下示例说明了 JavaScript 中的**符号不可访问属性**:

**示例 1:** 如果所有属性都设置为假。

```
// JavaScript to illustrate Symbol.toPrimitive  
var obj1 = {   
  val: "Have",   
  val1: "FUN"
};  
obj1[Symbol.unscopables] = {     
  val1: false,      
  val: false   
};  
with (obj1) {  
  console.log(val1);  
}  
with (obj1) {  
  console.log(val);  
}
```

**输出:**

```
> "FUN"
> "Have"

```

**示例 2:** 如果任何属性设置为真。

```
// JavaScript to illustrate Symbol.toPrimitive  
var obj1 = {   
  val: "Have",   
  val1: "FUN"
};  
obj1[Symbol.unscopables] = {     
  val1: false,      
  val: true   
};  
with (obj1) {  
  console.log(val1);  
}  
with (obj1) {  
  console.log(val);  
}
```

**输出:**

```
"FUN"
Error: val is not defined

```

**例 3:**

```
var list = [];

with (Array.prototype) {
  list.push('unscopables');
}

console.log(Object.keys(Array.prototype[Symbol.unscopables])); 
```

**输出:**

```
[
  'copyWithin', 'entries',
  'fill',       'find',
  'findIndex',  'flat',
  'flatMap',    'includes',
  'keys',       'values'
]

```

**支持的浏览器:**JavaScript**符号不可访问属性**支持的浏览器如下:

*   谷歌 Chrome 45
*   边缘 12 及以上
*   Firefox 48 及以上版本
*   歌剧 32 及以上
*   Safari 9 及以上

**参考:**[https://devdocs . io/JavaScript/global _ objects/symbol/unscopedables](https://devdocs.io/javascript/global_objects/symbol/unscopables)