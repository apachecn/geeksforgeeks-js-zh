# Moment.js moment()。diff()功能

> 原文:[https://www . geesforgeks . org/moment-js-moment-diff-function/](https://www.geeksforgeeks.org/moment-js-moment-diff-function/)

**时刻()。diff()** 函数用于获取给定日期的差异(以毫秒为单位)，这些日期作为参数传递给该函数。

**语法:**

```
moment().diff(Moment|String|Number|Date|Array, String, Boolean);
```

**参数:**这个函数有两个参数，第一个是 Moment | String | Number | Date | Array 类型的日期，第二个参数是 boolean 类型的可选参数，用于获取浮点数作为结果，而不是整数。

**返回值:**该函数以毫秒为单位返回日期。

**力矩模块安装:**

1.  您可以访问[安装力矩模块](https://www.npmjs.com/package/moment)的链接。您可以使用此命令安装此软件包。

    ```
    npm install moment
    ```

2.  安装力矩模块后，可以使用命令在命令提示符下检查您的**力矩**版本。

    ```
    npm version moment
    ```

3.  之后，您可以创建一个文件夹并添加一个文件，例如 index.js，如下所示。

**示例 1:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

var dateOne = moment([2019, 03, 17]);
var dateTwo = moment([2001, 10, 28]);

// Function call
var result = dateOne.diff(dateTwo, 'days') 

console.log("No of Days:", result)
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/3209d9b4369c180282a34be8070d7d6e.png)
2.  Run **index.js** file using below command:

    ```
    node index.js
    ```

    **输出:**

    ```
    No of Days: 6349

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function getYearDiff(dateOne, dateTwo) {
   return dateOne.diff(dateTwo, 'years', true);
}

// Function call
var result = getYearDiff(moment([2019, 11, 
    30]), moment([2001, 2, 17]));

console.log("No of years difference:", result)
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/3209d9b4369c180282a34be8070d7d6e.png)
2.  Run **index.js** file using below command:

    ```
    node index.js
    ```

    **输出:**

    ```
    No of years difference: 18.78611111111111

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/difference/