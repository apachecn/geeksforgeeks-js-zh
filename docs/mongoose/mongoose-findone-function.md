# 猫鼬| findOne()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-findone-function/](https://www.geeksforgeeks.org/mongoose-findone-function/)

**findOne()功能**用于根据条件查找一个单据。如果多个文档匹配该条件，则返回满足该条件的第一个文档。

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

```
const mongoose = require('mongoose');

// Database connection
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

// Find only one document matching
// the condition(age >= 5)
User.findOne({age: {$gte:5} }, function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Result : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/e86137718bde456f11d692860c6c0166.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是执行函数之前数据库中的示例数据。您可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/aea0c805d8c7a20554c7b60d12dbce50.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/e82a7066ea67d956d5156c8173e58c0d.png)

这就是如何使用 mongoose findOne()函数，根据条件找到一个文档。如果多个文档匹配该条件，则返回满足该条件的第一个文档。