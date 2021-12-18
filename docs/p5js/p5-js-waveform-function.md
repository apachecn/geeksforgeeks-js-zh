# p5.js |波形()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-waveform-function/](https://www.geeksforgeeks.org/p5-js-waveform-function/)

**波形()函数**是 p5.js 库中的一个内置函数。该函数用于返回振幅值，这将是单个缓冲器中振幅读数的快照。这可以用来绘制声音的波形。

**语法:**

```
waveform(bins, precision)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **箱:**该参数用于保存一个整数，该整数将像 2 <sup>n</sup> 一样表示。范围是 16 到 1024，默认值是 1024，是可选参数。
*   **精度:**该参数用于返回 Float32 数组，如果前一个参数保持任何值，该数组比常规数组更精确。它也是一个可选的。

下面的例子说明了 JavaScript 中的 **p5.waveform()函数**:
**例子:**

```
var sound; 
var wvfrm;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();

    // will return no of frames
    wvfrm = sound.waveform();
    console.log(wvfrm);
} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js 波形()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧