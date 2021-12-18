# JavaScript | handler.ownKeys()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-own keys-method/](https://www.geeksforgeeks.org/javascript-handler-ownkeys-method/)

JavaScript 中的 **handler.ownKeys()** 方法是 **Reflect.ownKeys()** 方法的陷阱，该方法返回一个可枚举对象。
**语法:**

```
const p = new Proxy(target, {
  ownKeys: function(target) {
  }
});
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **目标:**此参数保存目标对象。

**返回值:**这个方法总是返回一个可枚举的对象。
以下示例说明了 JavaScript 中的 **handler.ownKeys()方法【T4:
**示例 1:**** 

## java 描述语言

```
const monster1 = {
  prop1: 253,
  prop2: "Geeks",
  prop3: 0101011
}

const handler1 = {
  ownKeys (target) {
    return Reflect.ownKeys(target)
  }
}

const proxy = new Proxy(monster1, handler1);

for (let key of Object.keys(proxy)) {
  document.writeln(key+"<br>");
}
```