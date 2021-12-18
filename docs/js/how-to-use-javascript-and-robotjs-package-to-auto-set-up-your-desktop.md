# 如何使用 Javascript 和 Robotjs 包自动设置桌面？

> 原文:[https://www . geeksforgeeks . org/如何使用 JavaScript-and-robotjs-package-to-auto-setup-your-desktop/](https://www.geeksforgeeks.org/how-to-use-javascript-and-robotjs-package-to-auto-set-up-your-desktop/)

本文展示了在 Robotjs 包和 JavaScript 的帮助下使用自动化设置桌面的方法。必须遵循以下步骤。

**步骤 1:** 从[这里](https://nodejs.org/en/download/)安装最新的 Node.js 运行时。

**步骤 2:** 安装[机器人](http://robotjs.io/docs/syntax)包。我们将在本地安装这个包，即它只能在工作文件夹中访问。这可以通过在安装节点的同一目录中打开终端/命令提示符并运行以下命令来完成。

```
npm install robotjs
```

**步骤 3:** 在与凭证文件相同的目录下创建一个 JavaScript 文件。该文件将包含用于控制操作系统和自动化所需任务的代码。按照下面的步骤做同样的事情。这是写在这个主 JavaScript 文件中的。

1.  去搜索栏。
2.  键入“openboard”并按 enter 打开它，然后最小化它。
3.  再次进入搜索栏。
4.  键入“升华文本”并按回车键打开它，然后最小化它。
5.  再次进入搜索栏。
6.  键入“chrome”并按 enter 打开它。打开“whatsapp web”和“gfg pratice”标签，然后最小化它。
7.  再次进入搜索栏。
8.  键入“一个音符”并按 enter 打开它，然后最小化它。
9.  再次进入搜索栏。
10.  键入“记事本”并按 enter 打开它，然后写一条“完成”消息

**步骤 4:** 使用下面的命令启动包含脚本的 JavaScript 文件。

```
node automate.js
```

**完整代码:**

## java 描述语言

```
// Include the robotjs package 
var robot = require("robotjs"); 
// Timeout to wait if system is slow 
setTimeout(startOpenBoard, 1000);

//Opening the openboard
//Can learn more about these
//properties from the robotjs site

function startOpenBoard(){
    robot.moveMouseSmooth(98,844);
    robot.mouseClick();
    robot.typeString(" openboard ");
    robot.keyTap("enter");

    //Minimize openboard
    robot.moveMouseSmooth(1433,28);
    robot.mouseClick();

    //Start sublime text after 1s
    setTimeout(startSublimeText, 1000);
}

function startSublimeText(){
    robot.moveMouseSmooth(98,844);
    robot.mouseClick();
    robot.typeString(" sublime text ");
    robot.keyTap("enter");

   //Minimize sublime
    robot.moveMouseSmooth(1418,8);
    robot.mouseClick();

    //Start chrome after 1s
    setTimeout(startChrome, 1000);
}

function startChrome(){
    robot.moveMouseSmooth(98,844);
    robot.mouseClick();
    robot.typeString(" chrome ");
    robot.keyTap("enter"); 

    //Open whatsapp web
    robot.moveMouseSmooth(506,516);
    robot.mouseClick();
    robot.typeString("whatsapp web");
    robot.keyTap("enter"); 

    robot.moveMouseSmooth(349,389);
    robot.mouseClick();

    //Open a new tab
    robot.keyToggle("control","down");
    robot.keyTap("t");
    robot.keyToggle("control","up");

    //Open gfg practice
    robot.moveMouseSmooth(506,516);
    robot.mouseClick();
    robot.typeString("gfg practice");
    robot.keyTap("enter"); 

    robot.moveMouseSmooth(362,788);
    robot.mouseClick();

    //Open a new tab
    robot.keyToggle("control","down");
    robot.keyTap("t");
    robot.keyToggle("control","up");

    //Minimize chrome
    robot.moveMouseSmooth(1398,23);
    robot.mouseClick();

    //Start one note after 1s
    setTimeout(startOneNote, 1000); 
} 

function startOneNote(){
    robot.moveMouseSmooth(98,844);
    robot.mouseClick();
    robot.typeString(" oneNote ");
    robot.keyTap("enter"); 

    //Minimize onr note
    robot.moveMouseSmooth(1443,10);
    robot.mouseClick();

    //Start notepad after 1s
    setTimeout(startNotePad, 1000);
}

function startNotePad(){
    robot.moveMouseSmooth(98,844);
    robot.mouseClick();
    robot.typeString(" notepad ");
    robot.keyTap("enter");
    robot.moveMouseSmooth(600,500);
    robot.mouseClick(); 
    //Type a "Set up done" message
    robot.typeString(" Your System is ready to use, Sir.");
}
```

**输出:**

<video class="wp-video-shortcode" id="video-566808-1" width="665" height="374" loop="1" autoplay="" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20210302133422/VID-20210302-WA0001.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20210302133422/VID-20210302-WA0001.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20210302133422/VID-20210302-WA0001.mp4)</video>

**注意:**这里我已经根据我的屏幕大小使用了坐标。人们可以通过运行下面的代码并把鼠标指向要寻找坐标的位置来找到他们的屏幕坐标。

运行以下命令:

```
node screenPosition.js
```

**代码:**

## java 描述语言

```
//Include robotjs package
var robot = require("robotjs");

//Show mouse location wherever it is pointing  
var id = setInterval(showMouseLocation,1000);

//function that
function showMouseLocation(){
var mousePosition = robot.getMousePos();
console.log(mousePosition);
//Terminate the program 
//whenever mouse points
//at top left corner
//or press ctrl+c to terminate
if(mousePosition.x == 0 && mousePosition.y == 0){
    clearInterval(id);  
}
}
```