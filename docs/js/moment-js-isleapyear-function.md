# moment . js islapyear()功能

> 原文:[https://www . geesforgeks . org/moment-js-islapy ear-function/](https://www.geeksforgeeks.org/moment-js-isleapyear-function/)

用于在 Moment.js 中使用**islapyear()**函数检查给定年份是否为闰年，如果该年份为闰年，则返回 true，否则返回 false。

**语法:**

```
moment().isLeapYear();

```

**参数:**不需要参数。

**返回:**真或假

**力矩模块安装:**

1.  您可以访问[安装力矩模块](https://www.npmjs.com/package/moment)的链接。您可以使用此命令安装此软件包。

    ```
    npm install moment
    ```

2.  安装**时刻**模块后，可以使用命令在命令提示符下检查您的**时刻**版本。

    ```
    npm version moment
    ```

3.  之后，您可以创建一个文件夹并添加一个文件，例如 **index.js** 。要运行此文件，您需要运行以下命令。

    ```
    node index.js
    ```

**示例 1:** **文件名:index.js**

```
// Requiring module
const moment = require('moment');

var bool1 = moment([2000]).isLeapYear() // true
console.log(bool1);
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/3209d9b4369c180282a34be8070d7d6e.png)
2.  使用以下命令确保您已经安装了**时刻**模块:

    ```
    npm install moment
    ```

3.  Run index.js file using below command:

    ```
    node index.js
    ```

    **输出:**

    ```
    true

    ```

**示例 2:** **文件名:index.js**

```
// Requiring module
const moment = require('moment');

function checkLeapYear(year){
   return moment([year]).isLeapYear();
}

var bool = checkLeapYear(2001)
console.log(bool);
```

使用以下命令运行 index.js 文件:

```
node index.js
```

**输出:**

```
false

```

**参考:**T2】https://momentjs.com/docs/#/query/is-leap-year/