# Moment.js moment()。日月()功能

> 原文:[https://www . geesforgeks . org/moment-js-moment-days in month-function/](https://www.geeksforgeeks.org/moment-js-moment-daysinmonth-function/)

**时刻()。daysInMonth()** 函数用于获取 Node.js 中某个特定月份的月天数，返回一个表示天数的整数。

**语法:**

```
moment().daysInMonth();
```

**参数:**此功能无参数。

**返回值:**此函数返回整数。

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
var result = moment("2020-02", "YYYY-MM").daysInMonth() 

console.log("No of days in 2020-02 is:", result)
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
    No of days in 2020-02 is: 29

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function getNoOfDays(date) {
   return moment(date, "YYYY-MM").daysInMonth() 
}

// Function call
var result = getNoOfDays("2019-03");
console.log("No of days in given date is:", result)
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
    No of days in given date is: 31

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/days-in-month/