# 猫鼬|更新()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-update-function/](https://www.geeksforgeeks.org/mongoose-update-function/)

**更新()功能**用于更新数据库中的一个文档而不返回。

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

User.update({name:"Gourav"}, function (err, result) {
    if (err){
        console.log(err)
    }else{
        console.log("Result :", result) 
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/39b1615d8c17199ce09af77e1fe5b683.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/af445ee8431acb062b891165c29e80f7.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/9466ee0930bf907a4ccb6a402dd800b2.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/215ea9fb59bc182f87cd59639b6f833d.png)

这就是如何使用 mongoose update()函数，该函数更新数据库中的一个文档而不返回它。