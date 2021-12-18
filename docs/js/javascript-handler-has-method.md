# JavaScript | handler.has()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-has-method/](https://www.geeksforgeeks.org/javascript-handler-has-method/)

JavaScript 中的 **handler.has()** 方法用来“隐藏”任何你想要的属性。对操作员来说，这是一个陷阱。它返回布尔值。
**语法:**

```
const p = new Proxy(target, {
  has: function(target, prop) {
  }
});
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **目标:**此参数为目标对象。
*   **道具:**这个参数是将要被检查是否存在的属性。

**返回值:**如果想要访问属性，这个方法返回一个布尔值 true。
以下示例说明了 JavaScript 中的 handler.has()方法:
**示例 1:**

## java 描述语言

```
<script>
const handler1 = {
  has (target, key) {
    if (key[1] === '1') {
      return false;
    }
    return key in target;
  }
};

const monster1 = {
  p1roperty1: 'GeeksforGeeks',
  property2: 4
};

const proxy1 = new Proxy(monster1, handler1);
console.log('property2' in proxy1);
console.log('p1roperty1' in proxy1);
console.log('p1roperty1' in monster1);
</script>
```

**输出:**

```
true
false
true
```

**例 2:**

## java 描述语言

```
<script>
var s={ 
  value:1 
} 
var p = new Proxy(s, { 
  has: function(target, prop) { 
    console.log( prop); 
    return false; 
  } 
}); 
console.log('prop' in p);

var p1 = new Proxy(s, { 
  has: function(target, prop) { 
    console.log( prop); 
    return true; 
  } 
}); 
console.log('prop' in p1);
</script>
```

**输出:**

```
"prop"
false
"prop"
true
```

**支持的浏览器:**handler . has()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 18 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上