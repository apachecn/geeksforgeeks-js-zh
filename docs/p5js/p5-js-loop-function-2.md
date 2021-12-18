# p5.js | loop()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-loop-function-2/](https://www.geeksforgeeks.org/p5-js-loop-function-2/)

**循环()函数**是 p5.js 库中的一个内置函数。此功能用于循环播放网络上的音频。循环函数可以在 play()函数之后或之前调用，这并不重要。它将循环播放加载的声音。

**语法:**

```
loop( startTime, rate, amp, cueStart, duration )
```

**注意:**所有与声音相关的功能只有当声音库包含在 index.html 文件的头段中时才起作用。

**参数:**该函数接受五个参数，如上所述，如下所述:

*   **开始时间:**此参数保存一个整数秒，用于定义计划的回放，是一个可选参数。
*   **速率:**该参数保存定义回放速率的整数，是可选参数。
*   **amp:** 该参数保存一个定义回放幅度的整数，是一个可选参数。
*   **cueStart:** 此参数保存一个以秒为单位的整数，以秒为单位定义提示开始时间，它是一个可选参数。
*   **持续时间:**该参数保存一个整数，以秒为单位定义播放持续时间，是可选参数。

下面给出的例子说明了 JavaScript 中的 **p5.js 循环()函数**:
**例子:**

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound in a loop
    sound.play(); 
    sound.loop();
} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js loop()函数**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧