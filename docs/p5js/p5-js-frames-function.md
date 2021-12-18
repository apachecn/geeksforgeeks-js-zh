# p5.js | frames()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-frames-function/](https://www.geeksforgeeks.org/p5-js-frames-function/)

**frames()函数**是 p5.js 库中的一个内置函数。该函数用于返回帧数。样本时间、持续时间和帧之间有一个简单的等式。公式为**帧=样本时间*持续时间**。

**语法:**

```
frames()
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**此功能不接受任何参数。

**返回值:**该函数返回一个包含帧数的整数。

下面的例子说明了 JavaScript 中的 **p5.frames()函数**:

**示例:**

```
var sound; 
var frm;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    // will return no of frames
    frm = sound.frames();
    console.log(frm);
} 
```

**输出:**

```
10201860 // no of frames of the played audio
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js frames()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧