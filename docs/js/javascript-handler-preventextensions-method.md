# JavaScript | handler . PrevenTextExtensions()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-handler-preventextensions-method/](https://www.geeksforgeeks.org/javascript-handler-preventextensions-method/)

JavaScript 中的**处理程序. preventexturents()**方法是**对象. preventexturents()**方法的陷阱，它返回一个布尔值。
**语法:**

```
const p = new Proxy(target, {
  preventExtensions: function(target) {
  }
});
```

**参数:**该方法接受保存目标对象的单参数**目标**。
**返回值:**这个方法返回一个布尔值。
下面的示例说明了 JavaScript 中的 handler.preventExtensions()方法:
**示例 1:**

## java 描述语言

```
<script>
const monster1 = {
  canEvolve: true
};

const handler1 = {
  preventExtensions(target) {
    target.canEvolve = false;
    Object.preventExtensions(target);
    return true;
  }
};

const proxy1 = new Proxy(monster1, handler1);

document.writeln(monster1.canEvolve);
document.writeln("<br>");
document.writeln(Object.preventExtensions(proxy1));
document.writeln("<br>");
document.writeln(monster1.canEvolve);
document.writeln("<br>");

const proxy = new Proxy({}, { 
   preventExtensions: function(target) { 
   Object.preventExtensions(target); 
   return !Object.isExtensible(target); 
  } 
}); 
document.writeln(Object.isExtensible(proxy));
</script>
```

**输出:**

```
true
[object Object]
false
true
```

**例 2:**

## java 描述语言

```
<script>
const p = new Proxy({}, {
  preventExtensions: function(target) {
    document.writeln('preventExtensions()'+"<br>");
    document.writeln(Object.preventExtensions(target)+"<br>");
    return true;
  }
});

document.writeln(Object.preventExtensions(p)+"<br>");

var x = { 
  first: false 
}; 
var y ={ 
  preventExtensions(target) { 
    target.canEvolve = false; 
    Object.preventExtensions(target); 
    return true; 
  } 
}; 
var proxy = new Proxy(x, y); 
document.writeln(x.first); 
Object.preventExtensions(proxy); 
document.writeln("<br/>"); 
document.writeln(x.first);
</script>
```

**输出:**

```
preventExtensions()
[object Object]
[object Object]
false
false
```

**支持的浏览器:**handler . preventextionss()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 22 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上