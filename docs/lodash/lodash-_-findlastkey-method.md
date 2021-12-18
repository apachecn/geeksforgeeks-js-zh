# Lodash _。findlastkey()方法〔t1〕

> 原文:[https://www.geeksforgeeks.org/lodash-_-findlastkey-method/](https://www.geeksforgeeks.org/lodash-_-findlastkey-method/)

洛达什 **_。findLastKey()方法** 就像的 _。findKey()方法不同的是它以相反的顺序迭代集合的元素。

**语法:**

```
_.findLastKey( object, predicate_function)

```

**参数:** 此方法接受两个参数，如上所述，如下所述:

*   **Object:** This parameter stores the object to be searched.
*   **Predicate _ Function:** The function called in each iteration.

**返回值:**这个方法 r 返回匹配元素的键，否则不定义。

**例 1**:

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'Ram':  { 'mark': 100, 'status': "pass" },
  'Shyam': { 'mark': 90, 'status': "pass" },
  'Arnav': { 'mark': 50,  'status': "fail" }
};

console.log(_.findLastKey(users, function(s) 
                { return s.mark > 80; }));

console.log(_.findLastKey(users, 
        { 'mark': 100, 'status': "pass" }));

console.log(_.findLastKey(users, 
        ['status', "fail"]));

console.log(_.findLastKey(users, 'status'));
```

**输出:**

```
Shyam
Ram
Arnav
Arnav

```

**示例 2:** 为不存在的值返回未定义。

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'Ram':  { 'mark': 100, 'status': "pass" },
  'Shyam': { 'mark': 90, 'status': "pass" },
  'Arnav': { 'mark': 50,  'status': "fail" }
};

console.log(_.findLastKey(users, function(s) 
        { return false; }));

console.log(_.findLastKey(users, 
        { 'mark': 100, 'status': "fail" }));

console.log(_.findLastKey(users, ['status', ""]));

console.log(_.findLastKey(users, 'mark'));
```

**输出:**

```
undefined
undefined
undefined
Arnav

```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 npm 安装 lodash 进行安装。