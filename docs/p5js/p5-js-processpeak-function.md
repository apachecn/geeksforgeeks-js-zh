# p5.js | processPeak()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-processpeak-function/](https://www.geeksforgeeks.org/p5-js-processpeak-function/)

**processPeak()函数**是 p5.js 库中的一个内置函数。该功能用于跟踪音频节拍。该函数在脱机音频环境中执行声音文件，并将该数据发送给回调函数。

该过程将加载的音频通过一个滤波器，该滤波器跟踪高于平均峰值的峰值。如果峰值低于平均峰值，则降低平均阈值。

**语法:**

```
processPeaks(callback, initThreshold, minThreshold, minPeaks)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受四个参数，如上所述，如下所述:

*   **回调:**此参数是音频到达缓冲区末尾时将调用的函数的名称。
*   **初始阈值:**该参数保存初始阈值。初始阈值默认为 0.9，是可选参数
*   **最小阈值:**该参数保持最小阈值。最小阈值默认为 0.22，它是可选参数
*   **最小峰值:**此参数保存最小峰值。最小峰值默认为 200，这是可选参数

下面的例子说明了 JavaScript 中的 **p5.processPeaks()函数**:

**示例:**

```
var sound; 
var ppeak;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    // will return no of frames
    ppeak = sound.processPeaks(gfg);
    console.log(ppeak);
} 

function gf(){
    alert("processPeaks function running")
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