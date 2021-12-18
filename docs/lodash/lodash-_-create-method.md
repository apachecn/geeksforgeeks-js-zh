# 洛达什 _。创建()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-create-method/](https://www.geeksforgeeks.org/lodash-_-create-method/)

洛达什 **_。create()方法**创建一个从原型对象继承的对象。如果给定了一个 properties 对象，它自己的可枚举字符串键控属性将被分配给创建的对象。

**语法:**

```
_.create( proto_obj, property_object)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **proto_obj:** 这是要继承的对象。
*   **property_object:** 这些是要分配给对象的属性。

**返回值:**这个方法返回一个新的对象。

**例 1:**

```
// Defining Lodash variable 
const _ = require('lodash'); 

function Geeks() {
  return true;
}

GFG = _.create(Geeks.prototype, {
  'GeeksforGeeks': "Computer Science Portal"
});

console.log(GFG);
```

**输出:**

```
Geeks { GeeksforGeeks: 'Computer Science Portal' }

```

**例 2:**

```
// Defining Lodash variable 
const _ = require('lodash'); 

function protoFunc() {
  return 'Geek';
}

GFG = _.create(protoFunc.prototype, {
  'a': "b"
});

console.log(GFG);
```

**输出:**

```
protoFunc { a: 'b' }
```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库，并且可以使用以下命令进行安装:

```
npm install lodash
```