# JavaScript | Reflect.apply()方法

> 原文:[https://www . geesforgeks . org/JavaScript-reflect-apply-method/](https://www.geeksforgeeks.org/javascript-reflect-apply-method/)

**Reflect.apply()方法**是 JavaScript 中的标准内置对象，用于使用指定的参数调用函数。它的工作原理类似于调用函数的**function . prototype . apply()**方法，但方式高效且易于理解。
**语法:**

```
Reflect.apply(target, thisArgument, argumentsList)
```

**参数:**该方法接受三个参数，如上所述，描述如下:

*   **目标:**该参数是将要调用的目标函数。
*   **此参数:**此参数具有调用目标函数所需的此值。
*   **ArgumentsList:** 此参数是一个类似数组的对象，用于指定调用目标的参数。

**返回值:**调用给定的目标函数导致指定的该值和参数。
**异常:**类型错误是当目标不可调用时作为结果给出的异常。
以下示例说明了 JavaScript 中的 **Reflect.apply()方法:
**示例 1:** 传递列表参数并创建字典对象。** 

## java 描述语言

```
function geeks1 (a, b, c) { 
    this.x = a; 
    this.y = b; 
    this.z = c; 
}const obj = {}; 
Reflect.apply ( geeks1 , obj, [12,42,32] ); 
console.log( obj ); 
```