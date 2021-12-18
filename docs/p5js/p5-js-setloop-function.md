# p5.js | setLoop()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-setloop-function/](https://www.geeksforgeeks.org/p5-js-setloop-function/)

**setLoop()函数**是 p5.js 库中的一个内置函数。此功能用于在网络上循环播放音频，您可以在播放加载的声音时更改该值，这将影响当前播放的结束时间。

**语法:**

```
setLoop( Boolean )
```

**注意:**所有与声音相关的功能只有当声音库包含在 index.html 文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **布尔值:**我们都知道布尔值的意思是真或假，这个参数可以将布尔值判断为真或假。

下面给出的例子说明了 **p5.js setLoop()函数**在 JavaScript 中:
**例子 1:** 这个例子将播放循环中的音频设置为 setLoop(true)。

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound in a loop
    sound.play(); 
    sound.setLoop(true);
} 
```

**示例 2:** 本示例将播放声音单次 setLoop(false)设置为。

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play(); 
    sound.setLoop(false);
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