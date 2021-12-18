# Moment.js isSameOrBefore()函数

> 原文:[https://www . geesforgeks . org/moment-js-issameorbefore-function/](https://www.geeksforgeeks.org/moment-js-issameorbefore-function/)

使用 **isSameOrBefore()** 函数检查某个时刻是否在另一个时刻之前或与另一个时刻相同，它用于检查 Moment.js 中某个日期是否在某个特定日期之前。第一个参数将被解析为一个时刻，如果还没有的话。

**语法:**

```
moment().isSameOrBefore(Moment|String|Number|Date|Array);
moment().isSameOrBefore(Moment|String|Number|Date|Array, String);

```

**参数:**可以是持有时刻|字符串|数字|日期|数组。

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

var bool1 = moment('2010-10-20')
    .isSameOrBefore('2010-10-21');  // true
console.log(bool1);

var bool2 = moment('2010-10-20')
    .isSameOrBefore('2010-10-20');  // true
console.log(bool2);

var bool3 = moment('2010-10-20')
    .isSameOrBefore('2010-10-19');  // false
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
    true
    true
    false

    ```

**示例 2:** **文件名:index.js**

```
// Requiring module
const moment = require('moment');

function checkIsSameOrBefore(date1, date2) {
   return moment(date1).isSameOrBefore(date2);  
}

var bool = checkIsSameOrBefore
    ('2009-10-20', '2010-10-20');  // true
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

**参考:**T2】https://momentjs.com/docs/#/query/is-same-or-before/