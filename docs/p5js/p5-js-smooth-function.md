# p5.js | smooth()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-smooth-function/](https://www.geeksforgeeks.org/p5-js-smooth-function/)

**smooth()函数**是 p5.js 库中的一个内置函数。该功能用于通过对最后一个分析帧求平均值来获得平滑的振幅分析。默认情况下，该功能处于关闭状态。

**语法:**

```
smooth(channel)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **设置:**该参数用于设置平滑度 0.0 < = 1.0

下面的例子说明了 JavaScript 中的 **p5.smooth()函数**:

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // using the smooth function
    sound.smooth(0.5);

    // Playing the preloaded sound 
    sound.play();
} 

```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js smooth()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧