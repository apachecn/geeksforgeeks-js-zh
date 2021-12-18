# 洛达什 _。函数 In()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-functionsin-method/](https://www.geeksforgeeks.org/lodash-_-functionsin-method/)

**洛达什**T2。functionsIn()方法 c 根据给定对象的自身和继承的可枚举属性创建一个函数属性名称数组。

**语法:**

```
_.functionsIn( object )

```

**参数:** 该方法接受两个参数，如上所述，如下所述:

*   **Object:** This is the object to be checked.

**返回值:**这个方法返回一个属性数组。

**例 1:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Defining object function
function GFGfunc() {
  this.Geek1 = _.constant('gfg');
  this.Geek2 = _.constant('gfg');
}

// Use of function
console.log(_.functionsIn(new GFGfunc));
```

**输出:**

```
[ 'Geek1', 'Geek2' ]

```

**例二:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Defining object function
function GFGfunc() {
  this.Geek1 = _.constant('gfg');
  this.Geek2 = _.constant('gfg');
}

GFGfunc.prototype.Geek3 = _.constant('gfg');

// Use of function
console.log(_.functionsIn(new GFGfunc));
```

**输出:**

```
[ 'Geek1', 'Geek2', 'Geek3' ]

```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 **npm 安装 lodash** 进行安装。