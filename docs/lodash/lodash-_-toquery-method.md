# 洛达什 _。toQuery()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-toquery-method/](https://www.geeksforgeeks.org/lodash-_-toquery-method/)

**洛达什 _。toQuery()方法**取一个对象，将其转换为等价的 URL 查询字符串。

**语法:**

```
_.toQuery( Object);

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **对象:**该方法取一个对象进行转换。

**返回值:**这个方法返回等价的 URL 查询字符串。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var s  = _.toQuery({ 
    name: 'GeeksforGeeks', 
    address: 'Noida',
    contact: '9876543210'
}); 

console.log("The generated URL Query String is : ", s);
```

**输出:**

```
The generated URL Query String is : 
name=GeeksforGeeks&address=Noida&contact=9876543210

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var s  = _.toQuery(
    { 'https://practice.geeksforgeeks.org/courses/?ref': 
    'gfg_header' });

console.log("The generated URL Query String is : ", s);
```

**输出:**

```
The generated URL Query String is : 
https%3A%2F%2Fpractice.geeksforgeeks.org%2Fcourses%2F%3Fref=gfg_header

```