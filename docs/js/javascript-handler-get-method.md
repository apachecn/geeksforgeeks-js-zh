# JavaScript | handler.get()方法

> 原文:[https://www . geesforgeks . org/JavaScript-handler-get-method/](https://www.geeksforgeeks.org/javascript-handler-get-method/)

JavaScript 中的 **handler.get()** 方法是获取属性值的陷阱。
**语法:**

```
const p = new Proxy(target, {
  get: function(target, property, receiver) {
  }
});
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**此参数保存目标对象。
*   **属性:**此参数保存要获取的属性的名称。
*   **接收器:**此参数保存代理或从代理继承的对象。

**返回值:**该方法返回任意值。
以下示例说明了 JavaScript 中的 handler.get()方法:
**示例 1:**

## java 描述语言

```
<script>
const monster1 = {
  string: 'Geeksforgeeks',
  num: 334
};

const handler1 = {
  get: function(target, prop, receiver) {
    if (prop === 'string') {
      return `${target.string.substr(0, 8)} ... Best portal!`;
    } else {
      return Reflect.get(...arguments);
    }
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(proxy1.num);
console.log(proxy1.string);
console.log(proxy1.numstring);

const obj = new Proxy({}, {
  get: function(target, property, receiver) {
    console.log('Property : ' + property);
    return 56.56;
  }
});

console.log(obj.value);
</script>
```

**输出:**

```
334
"Geeksfor ... Best portal!"
undefined
"Property : value"
56.56
```

**例 2:**

## java 描述语言

```
<script>
const obj = {};
Object.defineProperty(obj, 'a', {
  configurable: false,
  enumerable: false,
  value: 10,
  writable: false
});

const p = new Proxy(obj, {
  get: function(target, property) {
    return 10;
  }
});

console.log(p.a);

var datalist = {  
  "vala": 32, "valb": 7 } 
var get = new Proxy( 
  datalist,  { 
    get: function(y, idx) { 
         return y[idx] * 11  
    }   
  } 
) 

for(var z in get) { 
  console.log(z +" : "+ get[z]) 
} 
</script>
```

**输出:**

```
10
"vala : 352"
"valb : 77"
```

**支持的浏览器:**handler . get()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 18 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上