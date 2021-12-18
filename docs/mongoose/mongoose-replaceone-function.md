# 猫鼬|替换 One()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-replaceone-function/](https://www.geeksforgeeks.org/mongoose-replaceone-function/)

**replaceOne()函数**与 update()函数相同，只是 MongoDB 用给定文档替换现有文档(没有像$set 这样的原子操作符)。

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
    useUnifiedTopology: true,
    useFindAndModify: false
});

// User model
const User = mongoose.model('User', {
    name: { type: String },
    age: { type: Number }
});

// Find document matching the condition(age >= 5) 
// and replace first document with new document
// This function has 4 parameters i.e.
// filter, update, options, callback
User.replaceOne({age: {$gte:5} }, {name:"Anuj"},
          null, function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Original Doc : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/db45bf4700a65622f3e3fb2c9eeac575.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/8d6887189044e89f1237ca1576e294e5.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/7bb35079818871e22f7538c57a5c1ccf.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/71b6422cac80840fb2398ee89a02d1f5.png)

这就是如何使用 mongoose replaceOne()函数，该函数与 update()相同，只是 MongoDB 用给定的文档替换现有的文档(没有像$set 这样的原子操作符)。