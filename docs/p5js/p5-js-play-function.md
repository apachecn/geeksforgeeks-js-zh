# p5.js | play()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-play-function/](https://www.geeksforgeeks.org/p5-js-play-function/)

**play()函数**是 p5.js 库中的一个内置函数。此功能用于在网络上播放加载的音频。播放函数应该在 **loadSound()** 函数之后调用。如果你在此之前打电话，它没有什么可玩的，所以它会显示加载，不会发生任何其他事情。

**语法:**

```
play( startTime, rate, amp, cueStart, duration )
```

**参数:**该函数接受五个参数，如上所述，如下所述:

*   **开始时间:**此参数保存一个整数秒，用于定义计划的回放，是一个可选参数。
*   **速率:**该参数保存定义回放速率的整数，是可选参数。
*   **amp:** 该参数保存一个定义回放幅度的整数，是一个可选参数。
*   **cueStart:** 此参数保存一个以秒为单位的整数，以秒为单位定义提示开始时间，它是一个可选参数。
*   **持续时间:**该参数保存一个整数，以秒为单位定义播放持续时间，是一个可选参数。

下面给出的示例说明了 JavaScript 中的 **p5.js play()** 函数:
T3】示例:

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play(); 
} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**浏览器支持的 **p5.js play()** 功能如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧