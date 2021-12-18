# JavaScript | handler . getprototypeof()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-getprototypeof-method/](https://www.geeksforgeeks.org/javascript-handler-getprototypeof-method/)

JavaScript 中的 **handler.getPrototypeOf()** 方法是内部方法的陷阱。此方法返回与**对象相同的值。
**语法:**** 

```
const p = new Proxy(obj, {
  getPrototypeOf(target) {
  ...
  }
}); 
```

**参数:**

*   **目标:**目标物体。

**返回值:**这个方法总是返回一个对象，如果没有返回对象，就返回一个空值。
以下示例说明了 JavaScript 中的 handler.getPrototypeOf()方法:
**示例 1:**

## java 描述语言

```
<script>
const monster1 = {
  porp: 46
};

const monsterPrototype = {
  porp : 52
};

const handler = {
  getPrototypeOf(target) {
    return monsterPrototype;
  }
};

const proxy1 = new Proxy(monster1, handler);
console.log(Object.getPrototypeOf(proxy1) === monsterPrototype);
console.log(Object.getPrototypeOf(proxy1).porp);

var obj = {}; 
var p = new Proxy(obj, { 
    getPrototypeOf(target) { 
        return Array.prototype; 
    } 
}); 
console.log( 
    p instanceof Array   
); 
</script>
```

**输出:**

```
true
52
true
```

**例 2:** 触发此法陷阱的五种方式

## java 描述语言

```
<script>
const obj = {};
const p = new Proxy(obj, {
    getPrototypeOf(target) {
        return Array.prototype;
    }
});
document.writeln(Object.getPrototypeOf(p) === Array.prototype);
document.writeln("<br>");
document.writeln(Reflect.getPrototypeOf(p) === Array.prototype);
document.writeln("<br>");
document.writeln(p.__proto__ === Array.prototype);
document.writeln("<br>");
document.writeln(Array.prototype.isPrototypeOf(p));             
document.writeln("<br>");
document.writeln(p instanceof Array );
</script>
```

**输出:**

```
true
true
true
true
true
```

**例外类型:**

1.  **类型错误:“目标”不是对象或为空**
    **示例 1:**

## java 描述语言

```
<script>
 const obj = {};
const p = new Proxy(obj, {
    getPrototypeOf(target) {
        return 'Geeksforgeeks';
    }
});
console.log(Object.getPrototypeOf(p));
</script>
```

1.  **输出:**

```
Error: 'getPrototypeOf' on proxy: trap returned
neither object nor null
```

1.  **类型错误:期望相同的原型值**
    **示例 2:** 类型错误:期望相同的原型值

## java 描述语言

```
<script>
 const obj = Object.preventExtensions({});
const p = new Proxy(obj, {
    getPrototypeOf(target) {
        return {};
    }
});
console.log(Object.getPrototypeOf(p));
</script>
```

1.  **输出:**

```
Error: 'getPrototypeOf' on proxy: proxy target is non-extensible
but the trap did not return its actual prototype
```

**支持的浏览器:**handler . getprototypeof()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 79 及以上
*   Firefox 49 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上