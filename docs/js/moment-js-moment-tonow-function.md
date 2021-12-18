# Moment.js moment()。toNow()功能

> 原文:[https://www . geesforgeks . org/moment-js-moment-to now-function/](https://www.geeksforgeeks.org/moment-js-moment-tonow-function/)

**时刻()。toNow(Boolean)** 函数用于计算 Node.js 中到现在的时间，这个函数有时被称为 timeago 或相对时间。

**语法:**

```
moment().toNow(Boolean);
```

**参数:**该函数有一个可选的布尔类型参数，用于返回不带前缀的值。

**返回值:**此函数返回日期。

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
var result = moment([2010, 8, 24]).toNow();
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
    in 10 years

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function timeToNow(date){
   return moment([2011, 8, 24]).toNow(true);
}

// Function call
var result = timeToNow(moment);
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
    Result: 9 years

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/tonow/