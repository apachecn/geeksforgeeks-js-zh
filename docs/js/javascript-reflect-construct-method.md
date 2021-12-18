# JavaScript | reflect . construct()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-construct-method/](https://www.geeksforgeeks.org/javascript-reflect-construct-method/)

JavaScript 中的 **Reflect.construct()** 方法用于调用新的目标。它还增加了指定不同原型的选项。
**语法:**

```
Reflect.construct(target, argumentsList, newTarget)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **目标:**该参数是将要调用的目标函数。
*   **ArgumentsList:** 此参数是一个类似数组的对象，用于指定调用目标的参数。
*   **newTarget:** 为可选参数。应该使用其原型的构造函数。

**返回值:**该方法返回目标的新实例。
**异常:**当目标不是构造函数时，类型错误是作为结果给出的异常。
以下示例说明了 JavaScript 中的 Reflect.construct()方法:
**示例 1:**

## java 描述语言

```
function func1(a, b, c) {
  this.sum = a + b + c;
}

const args = [1, 2, 3];
const object1 = new func1(...args);
const object2 = Reflect.construct(func1, args);

console.log(object2.sum);

console.log(object1.sum);

function func2(a, b, c) { 
  this.sum = a + b + c; 
} 
const args2 = [1, 4, 3]; 
const args3 = [1, 2, 3]; 
const object3 = new func1(...args); 
const object4 = Reflect.construct(func2, args2); 
console.log(object4.sum); 
console.log(object3.sum); 
```

**输出:**

```
6
6
8
6
```

**例 2:**

## java 描述语言

```
function OneClass() {
    this.name = 'one'
}

function OtherClass() {
    this.name = 'other'
}
const args=[1, 2, 3];

let obj1 = Reflect.construct(OneClass, args, OtherClass)

let obj2 = Object.create(OtherClass.prototype)
OneClass.apply(obj2, args)

console.log(obj1.name)
console.log(obj2.name) 

console.log(obj1 instanceof OneClass)
console.log(obj2 instanceof OneClass)

console.log(obj1 instanceof OtherClass)
console.log(obj2 instanceof OtherClass)
```

**输出:**

```
"one"
"one"
false
false
true
true
```

**支持的浏览器:**JavaScript reflect . apply()方法支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 42 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上