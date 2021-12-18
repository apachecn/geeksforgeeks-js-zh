# JavaScript | handler.apply()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-apply-method/](https://www.geeksforgeeks.org/javascript-handler-apply-method/)

JavaScript 中的 **handler.apply()方法**被用作函数调用的陷阱。此方法返回的值用作通过代理调用函数的结果。
**语法:**

```
const p = new Proxy(target, {
  apply: function(target, thisArg, argumentsList) {
  }
});
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**此参数保存目标对象。
*   **此参数:**此参数用于呼叫。
*   **参数列表:**该参数包含列表作为参数，用于调用。

**返回值:**该方法返回任意值。
以下示例说明了 JavaScript 中的 handler.apply()方法:
**示例 1:**

## java 描述语言

```
function sum(a, b) {
  return a + b;
}

const handler = {
  apply: function(target, thisArg, argumentsList) {
    console.log(`Calculate sum: ${argumentsList}`);

    return target(argumentsList[0], argumentsList[1])*14/3;
  }
};

const proxy1 = new Proxy(sum, handler);

console.log(sum(23, 4));
console.log(proxy1(23, 4));
```

**输出:**

```
27
"Calculate sum: 23, 4"
126
```

**例 2:**

## java 描述语言

```
var str = function(arg1, arg2) { 
  console.log('geeks get (' + arg1 + ', ' + arg2 + ')'); 
}; 
var proxy = new Proxy(str, { 
  apply: function(target, thisArg, parameters) { 
   console.log('Geeksforgeeks'); 

    return target.apply(thisArg, parameters); 
  } 
}); 
proxy('Tutorial', 'Jobs'); 

proxy.apply(null, ['Knowledge', 'internships']); 
proxy.call(null, 'Stipend', 'skills');
```

**输出:**

```
"Geeksforgeeks"
"geeks get (Tutorial, Jobs)"
"Geeksforgeeks"
"geeks get (Knowledge, internships)"
"Geeksforgeeks"
"geeks get (Stipend, skills)"
```

**支持的浏览器:**JavaScript handler . apply()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 18 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上