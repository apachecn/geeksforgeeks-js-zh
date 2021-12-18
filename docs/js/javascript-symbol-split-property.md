# JavaScript | Symbol.split 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-split-property/](https://www.geeksforgeeks.org/javascript-symbol-split-property/)

JavaScript 中的 **Symbol.split** 属性是一个众所周知的符号，用于指定在匹配正则表达式的索引处拆分字符串的方法。这个函数由 **String.prototype.split()** 方法调用。

**语法:**

```
[Symbol.split](string)

```

**属性属性:**接受不可写、不可枚举、不可配置的“字符串”。
**返回值:**返回从给定表达式拆分的字符串。

以下示例说明了 JavaScript 中的**符号分割属性**:

**例 1:**

## java 描述语言

```
class Split1 {
  constructor(value) {
    this.value = value;
  }
  [Symbol.split](string) {
    const index = string.indexOf(this.value);
    return "'"+ string.substr(0, index) + "' '"
      + this.value + "' '"+ string.substr(index + this.value.length)+"'";
  }
}

console.log('GeeksforGeeks'.split(new Split1('for')));
console.log('Geeks1Geeks2Geeks3Geeks4'.split(new Split1('Geeks')));
```

**输出:**

```
> "'Geeks' 'for' 'Geeks'"
> "'' 'Geeks' '1Geeks2Geeks3Geeks4'"

```

**例 2:**

## java 描述语言

```
class Split1 {
  constructor(value) {
    this.value = value;
  }
  [Symbol.split](string) {
    const index = string.indexOf(this.value);
    return "_"+ string.substr(0, index) + "__"
      + this.value + "__"+ string.substr(index + this.value.length)+"_";
  }
}

document.write('GeeksforGeeks'.split(new Split1('for')));
document.write("<br>");
document.write('Computer Science Portal'.split(new Split1(' ')));
```

**输出:**

```
_Geeks__for__Geeks_
_Computer__ __Science Portal_

```

**支持的浏览器:**JavaScript**符号.拆分属性**支持的浏览器如下:

*   谷歌 Chrome 51
*   Firefox 50
*   边缘 15
*   歌剧
*   苹果 Safari

**参考:**T2https://devdocs.io/javascript/global_objects/symbol/split