# JavaScript | reflect . getprototypeof()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-getprototypeof-method/](https://www.geeksforgeeks.org/javascript-reflect-getprototypeof-method/)

JavaScript 中的 **Reflect.getPrototypeOf()** 方法用于返回指定对象的原型。
**语法:**

```
Reflect.getPrototypeOf( obj ) 
```

**参数:**该方法接受上述单个参数，描述如下:

*   **obj:** 这个参数是目标对象，用来得到原型。

**返回值:**这个方法用来获取返回的给定对象的原型。
**异常:**类型错误是当目标无效时作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.getPrototypeOf()方法:
**示例 1:**

## java 描述语言

```
<script>
const object1 = {
    property1: 356
};

const result = Reflect.getPrototypeOf(object1);
console.log(result);
console.log(Reflect.getPrototypeOf(result));

const result1 = Object.create (null); 
console.log ( 
 Reflect.getPrototypeOf ( result1 ) === null 
);  
</script>
```

**输出:**

```
Object {  }
null
true
```

**例 2:**

## java 描述语言

```
<script>
console.log (Reflect.getPrototypeOf({}));      
console.log (Reflect.getPrototypeOf(Object.prototype)); 
console.log (Reflect.getPrototypeOf(Object.create(null)));
</script>
```

**输出:**

```
Object {  }
null
null
```

**支持的浏览器:**JavaScript reflect . getprototypeof()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上