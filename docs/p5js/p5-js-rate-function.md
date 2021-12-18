# p5.js | rate()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-rate-function/](https://www.geeksforgeeks.org/p5-js-rate-function/)

**rate()函数**是 p5.js 库中的一个内置函数。该功能用于控制网络上播放音频的速度。这个速度也可以通过滑块在不同的范围内划分来控制。

**语法:**

```
rate( playbackRate )
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **播放速率:**此参数用于保存播放速度速率的值。

下面的例子说明了 JavaScript 中的 **p5.rate()函数**:

**Example 1:** In this example the audio will play 2x time faster than normal rate.

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //sound will play twice fast 
    sound.rate(2);
} 
```

**示例 2:** 在本例中，音频将以正常速度播放，但您可以更改。通过滑动滑块，滑块的每一步都会加快 0.2 倍。范围是 1 到 2，意味着正常速度要快 2 倍。

```
var sound; 
var speed; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    //creating speed rate slider
    speed = createSlider(1, 2, 1, 0.2);

} 

function draw() {
    sound.rate(speed.value());
}
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**功能支持的浏览器 **p5.js rate()** 如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧