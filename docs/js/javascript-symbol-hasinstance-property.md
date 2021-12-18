# JavaScript | symbol . has instance 属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-hasinstance-property/](https://www.geeksforgeeks.org/javascript-symbol-hasinstance-property/)

**符号. hasInstance** 是 JavaScript 中的一个内置属性，用于*确定给定的构造函数对象是否将该对象识别为其实例。*
**语法:**

```
[Symbol.hasInstance](Object)  
```

**参数:**接受一个参数**“对象”**。
**返回值:**如果值在对象链中，则返回 **true** 否则返回 false。
JavaScript 代码展示了这个函数的工作原理。
**示例-1:**

## java 描述语言

```
<script>
   // Initialising some objects
   var obj1 = [1, 2, 3];
   var obj2 = ['a', 'b', 'c'];
   var obj3 = [123];
   var obj4 = [];

   // Calling Symbol.hasInstance Property
   console.log( Array[Symbol.hasInstance](obj1));
   console.log( Array[Symbol.hasInstance](obj2));
   console.log( Array[Symbol.hasInstance](obj3));
   console.log( Array[Symbol.hasInstance](obj4));
</script>
```

**输出:**

```
> true
> true
> true
> true
```

**示例-2:**

## java 描述语言

```
<script>
    // Calling a user define function 
    function gfg() 
    {} 

    // Initialising the object
    var Script = new gfg 

    // Calling the Symbol.hasInstance property
    console.log(gfg[Symbol.hasInstance](Script));   
</script>
```

**输出:**

```
> true
```

**支持的浏览器:**

*   谷歌 Chrome 50 以上
*   火狐 50 以上
*   边缘 15 以上
*   歌剧 37 以上
*   Apple Safari 10 及以上版本

**参考:**T2【https://devdocs . io/JavaScript/global _ objects/symbol/hasinstanceT4】