# Moment.js isDate()函数

> 原文:[https://www.geeksforgeeks.org/moment-js-isdate-function/](https://www.geeksforgeeks.org/moment-js-isdate-function/)

给变量一个值，任务是使用 **isDate()** 方法检查一个变量是否是 Moment.js 中的实际日期。若要检查变量是否是本机 js Date 对象，请使用 moment.isDate()方法。

**语法:**

```
moment.isDate(obj);
```

**参数:**对象

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

var bool1 = moment.isDate(); // false
console.log(bool1);

var bool2 = moment.isDate(new Date()); // true
console.log(bool2);

var bool3 = moment.isDate(moment()); // false
console.log(bool3);
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
    false
    true
    false

    ```

**示例 2:** **文件名:index.js**

```
// Requiring module
const moment = require('moment');

function checkIsDate(obj) {
   return moment.isDate(obj);
}

var bool = checkIsDate(new Date());
console.log(bool);
```

使用以下命令运行 index.js 文件:

```
node index.js
```

**输出:**

```
true

```

**参考:**T2】https://momentjs.com/docs/#/query/is-a-date/