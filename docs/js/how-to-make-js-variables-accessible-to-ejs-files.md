# 如何制作。可访问的 js 变量。ejs 文件？

> 原文:[https://www . geesforgeks . org/how-to-make-js-variables-access-to-ejs-file/](https://www.geeksforgeeks.org/how-to-make-js-variables-accessible-to-ejs-files/)

**EJS** 是一种简单的模板语言，可以让你用普通的 JavaScript 生成 HTML 标记。可以在中访问 JS 变量。ejs 文件。

只需要将 JS 对象作为 [res.render()](https://www.geeksforgeeks.org/express-js-res-render-function/) 方法的第二个参数传递即可。让我们跳进深渊。

**项目结构:**最终文件夹结构如下图所示。

```
Project
|
|-> node_modules
|-> views
  |-> index.ejs
|-> package.json
|-> package-lock.json
|-> server.js
```

**第一步:**发起新的 Node JS 项目。打开命令提示符，创建一个新文件夹，并使用空的 npm 项目启动它。

```
mkdir Project
cd Project
npm init -y
```

**步骤 2:** 安装需要依赖关系。

**要求依赖关系:**

1.  快递 JS
2.  EJS

```
npm i express ejs
```

**步骤 3:** 在 Project 目录中创建新的 server.js 文件。该文件包含一个应用编程接口端点，负责呈现一个动态生成 HTML 标记的 EJS 文件。这里渲染方法采用两个参数。第一个参数是 EJS 文件，第二个参数是一个 JS 对象，它在。ejs 文件。

我们到了。**{ first name:“Geeks”，，lastName:“一个计算机科学门户”}** 作为 JS 对象。

## server.js

```
const express = require('express');
const path = require('path');    
const ejs = require('ejs');

const app = express();
const PORT = 3000;

// Set EJS as templating engine
app.set('view engine', 'ejs');

app.get('/', (req,res)=>{
    // render method takes two parameters
    // first parameter should be the .ejs file
    // second parameter should be an object
    // which is accessible in the .ejs file  
    // this .ejs file should be in views folder 
    // in the root directory.
    res.render('index.ejs', {firstName: "Geeks,", 
                             lastName: "A Computer Science Portal"});
})

// Start the server
app.listen(PORT, err =>{
    err ? 
    console.log("Error in server setup") :
    console.log("Server listening on Port", PORT)
});
```

**第 4 步:**EJS 的默认行为是查看“视图”文件夹中要渲染的模板。因此，让我们在我们的主节点项目文件夹中创建一个“视图”文件夹，并创建一个名为“ **index.ejs** 的文件，该文件将在我们的节点项目中为一些期望的请求提供服务。本页面内容为:

## 索引. ejs

```
<!DOCTYPE html>
<html>

<body style="text-align: center">
    <h1 style="color: green"> GeeksforGeeks </h1>
    <h3> 
        Welcome 
        <%= firstName %> 
        <%= lastName %> 
    </h3>
</body>
</html>
```

这里传递的对象将是析构函数。所以，我们可以直接访问对象属性而不需要使用点运算符。

**第 5 步:**在项目根目录下打开命令提示符，使用启动服务器

```
node server.js
```

**输出:**如果一切顺利，您将看到“服务器正在端口 3000 上侦听”。然后在浏览器上打开 **http://localhost:3000/** ，屏幕上会出现如下输出。

**输出:**
![](img/de7e6b210e47d8103a3b652db0b6bd73.png)

**使用数组。中的 js。ejs 文件:**我们也可以使用 ejs 文件中的数组作为变量，在这个例子中，它将一个 js 数组传递给 ejs 文件进行渲染。

## server.js

```
const author = {
    name : 'Geeksforgeeks',
    skills: ['DSA', 'Interview Experience', 'Web Developement', 'Puzzels',]
}

app.get('/', (req,res)=>{
    // render method takes two parameters
    // first parameter should be the .ejs file
    // second parameter should be an object
    // which is accessible in the .ejs file  
    // this .ejs file should be in views folder 
    // in the root directory.
    res.render('index.ejs', {author: author} );
})
```

## 索引. ejs

```
<!DOCTYPE html>
<html>

<body>
    <h1 style="color: green"> GeeksForGeeks </h1>
    <h3> 
        <%= author.name %> has skill on 
    </h3>

    <ul>
        <% author.skills.forEach((skill)=>{%>
              <li><%=skill%></li> 
        <%});%>
    </ul>

</body>
</html>
```

**输出:**

![](img/d22619cdba2393ca04783f9fbb150647.png)