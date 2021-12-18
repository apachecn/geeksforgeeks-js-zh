# 猫鼬|移除()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-remove-function/](https://www.geeksforgeeks.org/mongoose-remove-function/)

**移除()功能**用于根据条件从数据库中移除文档。

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

User.remove({age:{$gte:30}}, function (err, result) {
    if (err){
        console.log(err)
    }else{
        console.log("Result :", result) 
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/cbde06daf9111c92a972c145b651266f.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/5ac3d9454242c3963baa62146fb4b052.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/5f840c279698688a32e0d78dd853c21a.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/4f0d8892ad357fe9b07697176edb17ee.png)

这就是如何使用 mongoose remove()函数，该函数根据条件从数据库中删除文档。