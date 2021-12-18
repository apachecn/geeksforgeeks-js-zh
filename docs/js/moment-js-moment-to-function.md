# Moment.js moment()。至()功能

> 原文:[https://www.geeksforgeeks.org/moment-js-moment-to-function/](https://www.geeksforgeeks.org/moment-js-moment-to-function/)

**时刻()。to()** 功能在用户想要显示与现在以外的时间相关的时刻时使用。这个函数计算到 Node.js 中特定日期的时间

**语法:**

```
moment().to(Moment|String|Number|Date|Array, Boolean);
```

**参数:**这个函数有两个参数，第一个是代表日期的类型 Moment | String | Number | Date | Array，第二个是布尔类型的可选参数，用于从值中删除后缀。

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
var result = moment([2010, 8, 24]).to([2013, 8, 24]);
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
    in 3 years

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function timeTo(date){
   return moment([2011, 8, 24]).to([2017, 10, 29], true)
}

// Function call
var result = timeTo(moment);
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
    Result: 6 years

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/to/