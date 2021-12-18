# p5.js | pan()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-pan-function/](https://www.geeksforgeeks.org/p5-js-pan-function/)

**pan()函数**是 p5.js 库中的一个内置函数。该功能用于控制网络上播放音频的平移。该函数的范围在(-1)和(1)之间，前者表示左侧，后者表示右侧。这种平移也可以通过滑块在不同范围内进行划分来控制。

**语法:**

```
pan(panValue, timeFromNow)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **声相值:**该参数用于保持立体声声相值，可选。
*   **timeFromNow:** 该参数用于保存第二种格式的时间整数值，在该时间之后将发生定义事件，并且是可选的。

以下示例说明了 JavaScript 中的 **p5.pan()函数**:
**示例 1:** 在本例中，音频将在 4 秒钟后在您的左侧播放，然后在 4 秒钟后，在其余时间内将在右侧播放。

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("song.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //sound will play only left ear after 4 seconds 
    sound.pan(-1, 4);

    //sound will play only right ear after 8 seconds
    sound.pan(1, 8);
} 
```

**示例 2:** 在本例中，您可以通过滑块左右控制平移效果，反之亦然。首发将是 0，这意味着双方都将被打。

```
var sound; 
var panner; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //creating pan slider
    panner = createSlider(-1, 1, 0, 0.2);

} 

function draw() {
    sound.pan(panner.value());
}
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**T2 P5 . js pan()功能支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧