# p5.js | setBuffer()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-setbuffer-function/](https://www.geeksforgeeks.org/p5-js-setbuffer-function/)

**setBuffer()函数**是 p5.js 库中的一个内置函数。该功能用于用当前缓冲区重置缓冲区。

**语法:**

```
setBuffer( buf )
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **buf:** 此参数保存一个数组，数组 2 Float32 Arrays 将创建一个立体声源。1 将创建单声道信号源。

下面的例子说明了 JavaScript 中的 **p5.setBuffer()函数**:

**示例:**

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // reversebyffering the source
    sound.setBuffer(1);

    // Playing the preloaded sound 
    sound.play();
} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**T2 P5 . js setBuffer()功能支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧