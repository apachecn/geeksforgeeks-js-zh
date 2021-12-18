# 猫鼬|更新多人()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-updatemany-function/](https://www.geeksforgeeks.org/mongoose-updatemany-function/)

**updateMany()函数**与 update()相同，只是 MongoDB 会更新所有匹配过滤器的文档。当用户想根据条件更新所有文档时使用。

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

// Find all documents matching the
// condition(age>=5) and update all
// This function has 4 parameters i.e.
// filter, update, options, callback
User.updateMany({age:{$gte:5}}, 
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
    ![project structure](img/1077a5927d477737856e3d56ee198fb1.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/e3cd1461a0d1587d6c8b30f8ec11c95c.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/3653c9bd223f2da9fad357d1314e32b4.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/56e657477e14daa2800b80bdba3dc09d.png)

这就是如何使用 mongoose updateMany()函数，它与 update()相同，只是 MongoDB 会更新所有匹配过滤器的文档。当用户想要根据条件更新所有文档时使用。