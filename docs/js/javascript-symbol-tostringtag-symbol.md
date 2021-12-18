# JavaScript | symbol . tostringtag 符号

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-tostringtag-symbol/](https://www.geeksforgeeks.org/javascript-symbol-tostringtag-symbol/)

**Symbol.toStringTag** 是 JavaScript 中众所周知的符号和字符串值属性，在创建对象的默认字符串描述时使用*。*

**语法:**

```
Symbol.toStringTag
```

**参数:**这个不取任何参数。
**返回值:**返回字符串对象。

显示该函数工作情况的 JavaScript 代码。
**例-1:**

## java 描述语言

```
<script>
    // Illustrating Symbol.toStringTag 
    console.log(Object.prototype.toString.call('Geeks'));    
    console.log(Object.prototype.toString.call("Geeks"));    
    console.log(Object.prototype.toString.call([1, 2, 3, 4]));   
    console.log(Object.prototype.toString.call(5));        
    console.log(Object.prototype.toString.call(true));   
    console.log(Object.prototype.toString.call(false));   
    console.log(Object.prototype.toString.call(undefined));
    console.log(Object.prototype.toString.call(null)); 
</script>
```

**输出:**

```
> "[object String]"
> "[object String]"
> "[object Array]"
> "[object Number]"
> "[object Boolean]"
> "[object Boolean]"
> "[object Undefined]"
> "[object Null]"
```

**示例-2:**

## java 描述语言

```
<script>
    // Illustrating Symbol.toStringTag 
    class ToString {get [Symbol.toStringTag]() { 
       return 'GeeksforGeeks'; 
      } 
    }

    // Getting the string description of the object
    console.log(Object.prototype.toString.call(new ToString()));  
</script>
```

**输出:**

```
> "[object GeeksforGeeks]"
```

**支持的浏览器:**

*   谷歌 Chrome 49
*   Firefox 51
*   边缘 15
*   歌剧 36 及以上
*   Apple Safari 10 及以上版本

**参考:**[https://devdocs . io/JavaScript/global _ objects/symbol/tostringtag](https://devdocs.io/javascript/global_objects/symbol/tostringtag)