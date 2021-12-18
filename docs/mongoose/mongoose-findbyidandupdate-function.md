# 猫鼬| findByIdAndUpdate()函数

> 原文:[https://www . geesforgeks . org/mongose-findbyidandupdate-function/](https://www.geeksforgeeks.org/mongoose-findbyidandupdate-function/)

**findByIdAndUpdate()函数**用于查找匹配的文档，根据更新参数进行更新，传递任意选项，并将找到的文档(如有)返回回调。

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

// Find a document whose 
// user_id=5eb985d440bd2155e4d788e2 and update it
// Updating name field of this user_id to name='Gourav'
var user_id = '5eb985d440bd2155e4d788e2';
User.findByIdAndUpdate(user_id, { name: 'Gourav' },
                            function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Updated User : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/af674028056f80fd83d0f59fc0ffb1ac.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是执行函数之前数据库中的示例数据。您可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/aa6b02f3429702ed233bfc48b78cb61a.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/e65bfbcd67b18b31967bff8d529d2a2f.png)

5.  执行该功能后，您可以在数据库中看到特定用户被删除，如下所示:
    ![new Database](img/521bb91e539dc9c7bd9a13921b3d1fdf.png)

这就是如何使用 mongoose findByIdAndUpdate()函数，该函数查找匹配的文档，根据更新参数进行更新，传递任何选项，并将找到的文档(如果有)返回给回调。