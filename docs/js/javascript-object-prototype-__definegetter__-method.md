# JavaScript object . prototype . _ _ defineGetter _ _()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-prototype-_ _ define getter _ _-method/](https://www.geeksforgeeks.org/javascript-object-prototype-__definegetter__-method/)

**__defineGetter__()方法**用于将对象的属性绑定到一个函数，该函数将在查找指定属性时被调用。建议使用**对象初始值设定项语法**或**对象定义属性()应用编程接口**来代替此方法，因为它已被否决。

**语法:**

```
obj.__defineGetter__( prop, func )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **prop:** 它是一个字符串，包含要绑定到给定函数的属性的名称。
*   **好玩:**是查找属性时要调用的函数。

**返回值:**该方法返回未定义。

以下示例说明了 __defineGetter__()方法的用法:

**示例 1:** 使用 __defineGetter__()方法

## java 描述语言

```
let obj = {};
obj.__defineGetter__('printTen', function() {
    return 10;
});
console.log(obj.printTen);
```

**输出:**

```
10
```

**示例 2:** 使用符合标准的方式，使用对象初始化器语法和 object . defineperoperty()API。

## java 描述语言

```
// Using the get operator
let obj = {
    get printTen() { return 10; }
};
console.log(obj.printTen);

// Using Object.defineProperty
let obj1 = {};
Object.defineProperty(obj1, 'printTwo', {
  get: function() {
    return 2;
  }
});
console.log(obj1.printTwo);
```

**输出:**

```
10
2
```

**支持的浏览器:**

*   Chrome 1 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 11 及以上版本
*   Opera 9.5 及以上
*   Safari 3 及以上版本