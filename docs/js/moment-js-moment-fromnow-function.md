# Moment.js moment()。fromNow()功能

> 原文:[https://www . geesforgeks . org/moment-js-moment-from now-function/](https://www.geeksforgeeks.org/moment-js-moment-fromnow-function/)

**时刻()。fromNow()** 函数用于计算 Node.js 中从现在开始的时间，该函数返回从参数传入的日期开始的时间。

**语法:**

```
moment().fromNow(Boolean);
```

**参数:**该函数有一个可选的布尔参数，传递该参数可以得到不带后缀的值。

**返回值:**该函数返回计算的日期。

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

// Function call
var result = moment([2010, 8, 24]).fromNow();
console.log(result);
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
    10 years ago

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function timeFromNow(date){
   return moment([2015, 8, 24]).fromNow(true);
}

// Function call
var result = timeFromNow(moment);
console.log("Result:", result);
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
    Result: 5 years

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/fromnow/