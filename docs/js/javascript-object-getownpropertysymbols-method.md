# JavaScript | object . getowntpropertymars()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-getowntpropertymars-method/](https://www.geeksforgeeks.org/javascript-object-getownpropertysymbols-method/)

JavaScript 中的**object . Getownpropertysymbols()方法**是标准的内置对象，它返回给定对象中存在的所有符号属性的数组。
**语法:**

```
Object.getOwnPropertySymbols(obj)
```

**参数:**

*   **obj:** 该参数是要返回符号属性的对象。

**返回值:**这个方法返回一个所有符号属性的数组，这些属性对应于直接在给定对象中找到的属性。
这里是这个方法的例子
**例子 1:**

## java 描述语言

```
<script>
const object1 = {};
let vala = Symbol('geek1');
let valb = Symbol.for('geek2');

object1[vala] = 'localSymbol';
object1[valb] = 'globalSymbol';

const objectSymbols = Object.getOwnPropertySymbols(object1);
console.log(objectSymbols.length);

const object2 = {}; 
let a = Symbol('a'); 
let b = Symbol.for('b'); 
const objectSymbols1 = Object.getOwnPropertySymbols(object2); 
console.log(objectSymbols1.length);
</script>
```

**输出:**

```
2
0
```

**例 2:**

## java 描述语言

```
<script>
const object1 = {};
let vala = Symbol('geek1');
let valb = Symbol.for('geek2');
let valc = Symbol.for('geek3');

object1[vala] = 'localSymbol';
object1[valb] = 'globalSymbol';
object1[valc] = 'globalSymbol';

const objectSymbols = Object.getOwnPropertySymbols(object1);
console.log(objectSymbols.length);
console.log(objectSymbols);     
console.log(objectSymbols[0]);
console.log(objectSymbols[2]);
console.log(objectSymbols[1]);
</script>
```

**输出:**

```
3
Array [Symbol(geek1), Symbol(geek2), Symbol(geek3)]
Symbol(geek1)
Symbol(geek3)
Symbol(geek2)
```

**支持的浏览器:**

*   谷歌 Chrome 38 及以上
*   边缘 12 及以上
*   Firefox 36 及以上版本
*   歌剧 25 及以上
*   Safari 9 及以上