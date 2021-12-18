# JavaScript | generator . prototype . return()方法

> 原文:[https://www . geesforgeks . org/JavaScript-生成器-原型-返回-方法/](https://www.geeksforgeeks.org/javascript-generator-prototype-return-method/)

**generator . prototype . return()**方法是 JavaScript 中的一个内置方法，用于返回给定值并完成生成器。
**语法:**

```
gen.return( value );
```

**参数:**该方法接受上述单个参数，描述如下:

*   **值:**该参数保存要返回的值。

**返回值:**这个方法返回作为参数给它的值。
以下示例说明了 JavaScript 中的 Generator.prototype.return()方法:
**示例 1:**

## java 描述语言

```
function* GFG() {
  yield "GeeksforGeeks";
  yield "JavaScript";
  yield "Generator.prototype.next()";
}

const geek = GFG();
console.log(geek.next());
console.log(geek.next()); 
console.log(geek.return("Shubham  Singh"));     
console.log(geek.next());         
```