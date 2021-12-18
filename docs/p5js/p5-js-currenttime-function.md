# p5.js | currentTime()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-currenttime-function/](https://www.geeksforgeeks.org/p5-js-currenttime-function/)

**Currettime()函数**是 p5.js 库中的一个内置函数。该函数用于返回在网络上播放的第二种格式的声音文件的当前时间。如果已经调用了 reverseBuffer，那么当前时间将开始向后计数。
**语法:**

```
currentTime()
```

**注意:**所有与声音相关的功能只有当声音库包含在 index.html 文件的头段中时才起作用。

**参数:**本功能不接受任何参数。
**返回值:**此功能返回当前播放声音文件的时间。

下面的例子说明了 **p5.js currentTime()函数**在 JavaScript 中:
**例子 1:** 在这个例子中当前时间将为 0，调用当前时间后 hust play()函数就是这个原因。

```
var sound; 
var crntm;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //checking the current time 
    crntm = sound.currentTime();
    console.log(crntm);
} 
```

**示例 2:** 在本示例中，当您单击为当前时间分配的按钮时，将显示当前时间。该按钮触发 currentTime()功能。

```
var sound; 
var crntm;   

function preload() { 

    // Initialize sound 
    sound = loadSound("song.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //Creating button
    crntm = createButton("Current Time");
    crntm.mousePressed(Currenttime);
} 

function Currenttime() {

    //will display the current time by button 
    var crrnt = sound.currentTime();
    console.log(crrnt);
}
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**功能支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧