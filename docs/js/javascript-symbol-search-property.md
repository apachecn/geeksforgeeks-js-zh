# JavaScript | Symbol.search 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-search-property/](https://www.geeksforgeeks.org/javascript-symbol-search-property/)

JavaScript 中的 **Symbol.search** 属性是一个众所周知的符号，它决定了返回与正则表达式匹配的字符串中的索引的方法。这个函数由**string . prototype . search()**方法调用。

**语法:**

```
[Symbol.search](string)
```

**参数:**接受单参数“字符串”。

**返回值:**返回字符串匹配的位置，如果不匹配，将返回 **-1** 。

以下示例说明了 JavaScript 中的 Symbol.search 属性:

**例 1:**

```
// JavaScript example to illustrate
// Symbol.search property
class obj {
  constructor(value) {
    this.value = value;
  }
  [Symbol.search](string) {
    return string.indexOf(this.value);
  }
}

console.log('Geeksforgeeks'.search(new obj('Geek')));
console.log('Geeksforgeeks'.search(new obj('geek')));
```

**输出:**

```
> 0
> 8

```

**例 2:**

```
// JavaScript program to illustrate
// the Symbol.search property
class S {    
  constructor(value) {  
    this.value = value;  
  }  
  [Symbol.search](string) {  
    return string.indexOf(this.value);  
  }  
}  
console.log('GEEKSFORGEEKS'.search(new S('geek')));  
console.log('GEEKSFORGEEKS'.search(new S('Geek')));
```

**输出:**

```
-1
-1

```

**支持的浏览器:**symbol . search 属性支持的浏览器如下:

*   Google Chrome 50 and above
*   Firefox 49 and above
*   Edge 79 and above
*   Opera 37 and above
*   Apple Safari 10 and above

**参考:**T2】https://devdocs.io/javascript/global_objects/symbol/search