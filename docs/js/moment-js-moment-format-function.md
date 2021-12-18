# Moment.js moment()。格式()功能

> 原文:[https://www . geesforgeks . org/moment-js-moment-format-function/](https://www.geeksforgeeks.org/moment-js-moment-format-function/)

**时刻()。format()** 功能用于根据用户需要格式化日期。该格式可以以字符串形式提供，并作为参数传递给该函数。

**语法:**

```
moment().format(String);
```

**参数:**该函数接受字符串类型的单个参数，该参数定义了格式。

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

// The format() function to format the date 
var formatedDate = moment().format(
    "dddd, MMMM Do YYYY, h:mm:ss a");
console.log(formatedDate);
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
    Friday, July 17th 2020, 4:28:30 pm

    ```

**示例 2:** **文件名:index.js**

```
// Requiring the module
const moment = require('moment');

function format_Date(date){
   return moment().format("dddd, MMMM Do YYYY");
}

var result = format_Date(moment);
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
    Result: Friday, July 17th 2020

    ```

**参考:**T2】https://momentjs.com/docs/#/displaying/format/