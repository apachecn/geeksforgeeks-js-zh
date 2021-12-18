# JavaScript | handler . deleteproperty()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-delete property-method/](https://www.geeksforgeeks.org/javascript-handler-deleteproperty-method/)

JavaScript 中的 **handler.deleteProperty()** 方法是删除操作符的陷阱。如果删除成功，此方法返回布尔值。
**语法:**

```
const p = new Proxy(target, {
  deleteProperty: function(target, property) {
  }
});
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **目标:**此参数保存目标对象。
*   **属性:**此参数保存要删除的属性的名称。

**返回值:**该方法返回一个布尔值，该值指示属性是否被成功删除。
以下示例说明了 JavaScript 中的 handler.deleteProperty()方法:
**示例 1:**

## java 描述语言

```
const monster1 = {
  Color: 'Green'
};

const handler1 = {
  deleteProperty(target, prop) {
    if (prop in target) {
      delete target[prop];
      console.log(`${prop} is property which is removed`);
    }
  }
};

console.log(monster1.Color);

const proxy1 = new Proxy(monster1, handler1);
delete proxy1.Color;

console.log(monster1.Color);

var f = { bar: 'baz' }   
console.log('bar' in f) 

delete f.bar 
console.log('bar' in f)
```