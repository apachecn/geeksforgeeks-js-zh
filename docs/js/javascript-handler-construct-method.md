# JavaScript | handler . construct()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-construct-method/](https://www.geeksforgeeks.org/javascript-handler-construct-method/)

JavaScript 中的 **handler.construct()** 方法是新操作的陷阱，这个方法返回一个对象。
**语法:**

```
const p = new Proxy(target, {
  construct: function(target, argumentsList, newTarget) {
  }
});  
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**此参数保存目标对象。
*   **参数列表:**此参数保存构造函数的列表。
*   **newTarget:** 这个参数保存了最初调用的构造函数，上面的 p。

**返回值:**这个方法返回一个对象。
以下示例说明了 JavaScript 中的 handler.construct()方法:
**示例 1:**

## java 描述语言

```
<script>
function monster1(disposition) {
  this.disposition = disposition;
}

const handler1 = {
  construct(target, args) {
    console.log('Users at Geeksforgeeks are called');

    return new target(...args);
  }
};

const proxy1 = new Proxy(monster1, handler1);
console.log(new proxy1('Geeks').disposition);

var pro = new Proxy(function() 
                    {}, { 
  construct: function(objTarget, args, oldConstructor) { 
     return { Value : args[0] + " to anybody" }  
  } 
}) 

console.log(JSON.stringify(new pro("Hello "), null, ' ')) 
</script>
```

**输出:**

```
"Users at Geeksforgeeks are called"
"Geeks"
"{
 "Value": "Hello  to anybody"
}"
```

**例 2:**

## java 描述语言

```
<script>
const p = new Proxy(function() {}, {
  construct: function(target, argumentsList, newTarget) {
    console.log('Value: ' + argumentsList.join(', '));
    return { value: argumentsList[0] * 10 /3};
  }
});

console.log('New Value: ' +new p(4).value);
</script>
```

**输出:**

```
"Value: 4"
"New Value: 13.333333333333334"
```

**支持的浏览器:**handler . construct()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   Firefox 18 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上
*   边缘 12 及以上