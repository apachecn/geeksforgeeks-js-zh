# 猫鼬| updateOne()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-updateone-function/](https://www.geeksforgeeks.org/mongoose-updateone-function/)

**updateOne()功能**用于更新符合条件的第一个文档。此功能与 update()相同，只是它不支持多重或覆盖选项。

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

// Find all documents matching the condition
// (age >= 5) and update first document
// This function has 4 parameters i.e. 
// filter, update, options, callback
User.updateOne({age:{$gte:5}}, 
    {name:"ABCD"}, function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Updated Docs : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/b66799be49fb5efa8d0fda6181244e30.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/3684c0be0a1d572f6bb2af8692cf2144.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/ca00411b32cafbda8d402f64c4a586d3.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/e47842ed53363b32493ed4198dece49e.png)

这就是如何使用 mongoose updateOne()函数，该函数用于更新第一个符合条件的文档。此功能与更新()相同，只是它不支持多重或覆盖选项。