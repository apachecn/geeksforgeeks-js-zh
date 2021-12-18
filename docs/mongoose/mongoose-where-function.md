# 猫鼬| where()函数

> 原文:[https://www.geeksforgeeks.org/mongoose-where-function/](https://www.geeksforgeeks.org/mongoose-where-function/)

函数用于创建查询，应用传递的条件并返回查询。

**猫鼬模块安装:**

1.  您可以访问[安装猫鼬模块](https://www.npmjs.com/package/mongoose)的链接。您可以使用此命令安装此软件包。

    ```
    npm install mongoose
    ```

2.  安装猫鼬模块后，您可以使用命令在命令提示符下检查您的猫鼬版本。

    ```
    npm version mongoose
    ```

3.  之后，您可以创建一个文件夹并添加一个文件，例如 index.js。

    ```
    node index.js
    ```

**文件名:index.js**

*   ```
    const mongoose = require('mongoose');

    // Database Connection
    mongoose.connect('mongodb://127.0.0.1:27017/geeksforgeeks', {
        useNewUrlParser: true,
        useCreateIndex: true,
        useUnifiedTopology: true
    });

    // User model
    const User = mongoose.model('User', {
        name: { type: String },
        age: { type: Number }
    });

    User.where('age').gte(5).lte(200)
            .exec(function (err, result) {
        if (err){
            console.log(err)
        }else{
            console.log("Result :", result) 
        }
    });
    ```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/976fb0d2ae6bd08fb8c0afb67fe1ba86.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![](img/5e351f721a41e25b6ce36c2e6ef07c3e.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/c92d7859ed6c9a887d66a123fcb0ee1c.png)

这就是如何使用 mongoose where()函数，该函数创建一个查询，应用传递的条件，并返回查询。