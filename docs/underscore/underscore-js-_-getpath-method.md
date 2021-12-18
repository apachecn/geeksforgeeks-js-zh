# 下划线. js _。getPath()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-getpath-method/](https://www.geeksforgeeks.org/underscore-js-_-getpath-method/)

**_。getPath()** 方法用于根据给定键描述的路径，获取嵌套对象中任意深度的值。键可以以数组或点分隔字符串的形式给出。

**语法:**

```
_.getPath( Object_name, key_string|array );
```

**参数:**

*   **对象名称:**要从中搜索值的对象。
*   **key_string | array:** 要在给定对象中搜索的给定点分隔字符串或数组。

**返回值:**这个方法 r 返回一个从对象中搜索到的值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**示例 1:** 使用点分隔字符串获取值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : {
        GeeksforGeeks :  "Computer Science Portal for Geeks"
    }
};
var val = _.getPath( ob, "gfg.GeeksforGeeks" );

console.log(val);
```

**输出:**

```
Computer Science Portal for Geeks
```

**示例 2:** 使用数组获取值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : {
        GeeksforGeeks :  "Computer Science Portal for Geeks"
    }
};
var val = _.getPath( ob, ['gfg', 'GeeksforGeeks'] );

console.log(val);
```

**输出:**

```
Computer Science Portal for Geeks
```