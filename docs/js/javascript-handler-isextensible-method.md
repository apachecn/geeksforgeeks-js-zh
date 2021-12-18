# JavaScript | handler . iseextensible()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-isextensible-method/](https://www.geeksforgeeks.org/javascript-handler-isextensible-method/)

JavaScript 中的**handler . isextensable()**方法是**object . isextensable()**方法的陷阱，它返回一个布尔值。
**语法:**

```
const p = new Proxy(target, {
  isExtensible: function(target) {
  }
});
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **目标:**此参数为目标对象。

**返回值:**这个方法返回一个布尔值。
以下示例说明了 JavaScript 中的 handler.isExtensible()方法:
**示例 1:**

## java 描述语言

```
<script>
const monster1 = {
  canEvolve: true
};

const handler1 = {
  isExtensible(target) {
    return Reflect.isExtensible(target);
  },
  preventExtensions(target) {
    target.canEvolve = false;
    return Reflect.preventExtensions(target);
  }
};

const proxy1 = new Proxy(monster1, handler1);
document.writeln(Object.isExtensible(proxy1));
document.writeln("<br>");
document.writeln(monster1.canEvolve);
document.writeln("<br>");
document.writeln(Object.preventExtensions(proxy1));
document.writeln("<br>");
document.writeln(Object.isExtensible(proxy1));
document.writeln("<br>");
document.writeln(monster1.canEvolve); 
</script>
```

**输出:**

```
true
true
[object Object]
false
false
```

**例 2:**

## java 描述语言

```
<script>
const p = new Proxy({}, {
  isExtensible: function(target) {
    console.log('isExtensible method');
    return true;
  }
});

console.log(Object.isExtensible(p));

var a = { 
  canEvolve: true 
}; 
var b = {  
  isExtensible(target) { 
    return true; 
  }, 
   }; 
const proxy1 = new Proxy(a, b); 
console.log(Object.isExtensible(proxy1));
</script>
```

**输出:**

```
"isExtensible method"
true
true
```

**支持的浏览器:**handler . isextensible()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 31 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上