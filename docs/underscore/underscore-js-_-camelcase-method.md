# 下划线. js _。camelCase()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-camelcase-method/](https://www.geeksforgeeks.org/underscore-js-_-camelcase-method/)

**_。方法用于将破折号分隔的字符串转换为驼色大小写字符串**

**语法:**

```
_.camelCase( dashedString );
```

**参数:**

*   [T0】 dashedString: 【T1] This method uses dashes to separate strings.

**返回值:**这个方法 r 返回转换后的 camelCase 字符串。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var cml  = _.camelCase( "a-ab-abc" );

console.log("The calmelCase String is : ", cml);
```

**输出:**

```
The calmelCase String is :  aAbAbc
```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var cml  = _.camelCase( "geeks-for-geeks" );

console.log("The calmelCase String is : ", cml);
```

**输出:**

```
The calmelCase String is :  geeksForGeeks
```