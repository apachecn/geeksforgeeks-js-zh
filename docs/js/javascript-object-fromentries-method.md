# JavaScript | object . from entries()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-from entries-method/](https://www.geeksforgeeks.org/javascript-object-fromentries-method/)

JavaScript 中的 **Object.fromEntries()方法**是标准的内置对象，用于将键值对列表转换为对象。此方法返回一个新对象，该对象的属性由 iterable 的条目给出

**语法:**

```
Object.fromEntries( iterable )
```

**参数:**该方法接受单参数**可迭代**，它保存一个可迭代的，如数组或映射或其他实现可迭代协议的对象。

**返回值:**这个方法总是返回一个新的对象，它的属性由 iterable 的条目给出。

下面的例子说明了 JavaScript 中的 Object.fromEntries()方法:

**示例 1:** 将地图转换为对象。

```
const map1 = new Map([ ['big', 'small'], [1, 0] ]);
const geek = Object.fromEntries(map1);
console.log(geek);

const map2 = new Map(
    [['Geek1', 'Intern'],
    ['stipend', 'Works basis']]
);
const geek1 = Object.fromEntries(map2);
console.log(geek1); 
```

**输出:**

```
Object { 1: 0, big: "small" }
Object { Geek1: "Intern", stipend: "Works basis" }
```

**示例 2:** 将数组转换为对象。

```
const arr1 = [ ['big', 'small'], [1, 0], ['a', 'z' ]];
const geek = Object.fromEntries(arr1);
console.log(geek);

const arr2 = [ ['Geek1', 'Intern'], ['stipend', 'Works basis'] ];
const geek1 = Object.fromEntries(arr2);
console.log(geek1);
```

**输出:**

```
Object { 1: 0, big: "small", a: "z" }
Object { Geek1: "Intern", stipend: "Works basis" }
```

**示例 3:** 其他转换

```
const params = 'type=Get_the Value&geekno=34&paid=10';
const searchParams = new URLSearchParams(params);

console.log(Object.fromEntries(searchParams));

const object1 = { val1: 112, val2: 345, val3: 76 };
const object2 = Object.fromEntries(
  Object.entries(object1)
  .map(([ key, val ]) => [ key, val * 3 ])
);
console.log(object2); 
```

**输出:**

```
Object { type: "Get_the Value", geekno: "34", paid: "10" }
Object { val1: 336, val2: 1035, val3: 228 }
```

**支持的浏览器:**object . from entries()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   工业管理学(Industrial Engineering)
*   歌剧
*   旅行队
*   边缘