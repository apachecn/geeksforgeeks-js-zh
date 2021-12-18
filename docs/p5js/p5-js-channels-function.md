# p5.js | channels()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-channels-function/](https://www.geeksforgeeks.org/p5-js-channels-function/)

**channel()函数**是 p5.js 库中的一个内置函数。该功能用于显示当时在网络上播放的频道数量。现在有六种类型的声道，如下所述:

*   单声道的
*   立体声系统
*   远景立体声
*   4.1 环绕声
*   5.1 环绕声
*   7.1 环绕声

**语法:**

```
channels()
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**本功能不接受任何参数。

下面的例子说明了 **p5.js channels()函数**在 JavaScript 中:
T3】例子:

```
var sound; 
var chnnl;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    // checking channels of the audio
    chnnl = sound.channels();
    console.log(chnnl);

} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js channels()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧