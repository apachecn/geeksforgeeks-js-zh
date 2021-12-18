# JavaScript 类型错误–设置只包含 getter 的属性“x”

> 原文:[https://www . geesforgeks . org/JavaScript-type error-setting-getter-only-property-x/](https://www.geeksforgeeks.org/javascript-typeerror-setting-getter-only-property-x/)

这个 JavaScript 异常**只设置 getter 属性**只在严格模式下工作，如果用户试图为只指定了 getter 的属性设置一个新值，就会出现这个异常。

**消息:**

```
TypeError: Assignment to read-only properties is 
           not allowed in strict mode (Edge)
TypeError: setting getter-only property "x" (Firefox)
TypeError: Cannot set property "prop" of #<Object> 
           which has only a getter (Chrome)

```

**错误类型:**

```
TypeError

```

**错误原因:**用户试图为只定义了 getter 的属性设置新值。

**示例 1:** 在本例中，为对象定义了 getter 方法。不能直接访问属性。

## 超文本标记语言

```
<script>
"use strict";
function GFG_Fun() { 
  var temp = null; 
  Object.defineProperty(this, 'temp', { 
    get: function() {
      return temp; 
    }
  });
}
var obj = new GFG_Fun(); 
obj.temp;
obj.temp = 100; // Error here
</script>
```

**输出:**

```
TypeError: Cannot set property temp of 
#<GFG_Fun> which has only a getter

```

**示例 2:** 在本例中，getter 方法是为对象“Person”定义的。无法直接访问属性“年龄”。

## 超文本标记语言

```
<script>
"use strict";
function Person(ageP) { 
  var age = ageP; 
  Object.defineProperty(this, 'age', { 
    get: function() {
      return age; 
    }
  });
}
var p = new Person(22);
p.age = 30;  // TypeError
</script>
```

**输出:**

```
TypeError: Cannot set property age of 
#<Person> which has only a getter

```