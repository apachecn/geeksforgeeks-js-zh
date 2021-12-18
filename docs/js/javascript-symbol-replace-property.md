# JavaScript | Symbol.replace 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-replace-property/](https://www.geeksforgeeks.org/javascript-symbol-replace-property/)

JavaScript 中的 **Symbol.replace** 属性是一个众所周知的符号，用于确定替换字符串的匹配子字符串的方法。这个函数由**string . prototype . replace()**方法调用。

**语法:**

```
[Symbol.replace](string) 
```

**参数:**接受单参数“字符串”。

**返回值:**将返回一个新的字符串。

下面的例子说明了 JavaScript 中的符号替换属性:

**例 1:**

```
class Replace1 {
    constructor(value) {
        this.value = value;
    }

    [Symbol.replace](string) {
        return `${string} --> ${this.value}`;
    }
}

console.log('geeksforgeeks'.replace(
            new Replace1('GEEKSFORGEEKS')));

console.log('Article written by '.replace(
            new Replace1('Shubham Singh')));
```

**输出:**

```
> "geeksforgeeks --> GEEKSFORGEEKS"
> "Article written by  --> Shubham Singh"

```

**例 2:**

```
class Replace2 {  
    constructor(value) {  
        this.value = value;  
    }  

    [Symbol.replace](string) {  
        return `${string}`;  
    }  
}

var val = new Replace2("geeksforgeeks");  
console.log("Before: " + val.value);  
console.log("After: " + val.value
        .toUpperCase().replace(val.value));  

var val2 = new Replace2("Few Users");  
console.log("Before: " + val2.value);  
console.log("After: " + "Millions of Users"
        .replace(val2.value));
```

**输出:**

```
> "Before: geeksforgeeks"
> "After: GEEKSFORGEEKS"
> "Before: Few Users"
> "After: Millions of Users"

```

**支持的浏览器:**symbol . replace 属性支持的浏览器如下:

*   谷歌铬合金 51
*   Firefox 50
*   边缘 15
*   歌剧
*   苹果旅行队

**参考:**T2】https://devdocs.io/javascript/global_objects/symbol/replace