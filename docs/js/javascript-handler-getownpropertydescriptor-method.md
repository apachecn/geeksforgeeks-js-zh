# JavaScript | handler . getowntpropertysdescriptor()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-handler-getownpertysdescriptor-method/](https://www.geeksforgeeks.org/javascript-handler-getownpropertydescriptor-method/)

Javascript 中的**handler . getowntpropertysdescriptor()**方法是**object . getowntpropertysdescriptor()**方法的陷阱。如果属性作为目标对象的不可配置的自有属性存在，则不能将其报告为不存在。
**语法:**

```
const p = new Proxy(target, {
  getOwnPropertyDescriptor: function(target, prop) {
  }
});
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **目标:**此参数为目标对象。
*   **道具:**此参数是应该检索其描述的属性的名称。

**返回值:**此方法返回一个对象或未定义。
以下示例说明了 JavaScript 中的 handler . getowntpropertysdescriptor()方法:
**示例 1:**

## java 描述语言

```
<script>
const monster1 = {
  num: 4
};

const handler1 = {
  getOwnPropertyDescriptor(target, prop) {
    console.log(`Type : ${prop}`);

    return { configurable: true, enumerable: true, value: 5 };
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(Object.getOwnPropertyDescriptor(proxy1, 'num').value);
console.log(Object.getOwnPropertyDescriptor(proxy1, 'bool').enumerable);
</script>
```

**输出:**

```
> "Type : num"
> 5
> "Type : bool"
> true
```

**例 2:**

## java 描述语言

```
<script>
const p = new Proxy({ VAL: 20}, {
  getOwnPropertyDescriptor: function(target, prop) {
    console.log('Property : ' + prop);
    return { configurable: true, enumerable: true, value: 10 };
  }
});

console.log(Object.getOwnPropertyDescriptor(p, 'VAL').value);

const obj = { a: 10 };
Object.preventExtensions(obj);
const pval = new Proxy(obj, {
  getOwnPropertyDescriptor: function(target, prop) {
    return undefined;
  }
});

console.log(Object.getOwnPropertyDescriptor(pval));
</script>
```

**输出:**

```
> "Property : VAL"
> 10
> undefined
```

**支持的浏览器:**handler . getowntpropertysdescriptor()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 18 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上