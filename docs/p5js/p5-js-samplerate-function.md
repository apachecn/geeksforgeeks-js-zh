# p5.js | sampleRate()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-samplerate-function/](https://www.geeksforgeeks.org/p5-js-samplerate-function/)

**sampleRate()函数**是 p5.js 库中的一个内置函数。该函数用于获取每秒钟加载的音频样本数。音频的采样率以千赫或赫兹测量，**1000 赫兹= 1 千赫兹**。这是不可更改的，它取决于操作系统的声卡。

*   光盘的采样率为 44100 赫兹*   The sample rate for the DVDsis 48000Hz

    **语法:**

    ```
    sampleRate()
    ```

    **注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

    **参数:**此功能不接受任何参数

    **返回值:**该函数返回一个整数，保存网络上每秒播放的音频样本。

    下面的例子说明了 JavaScript 中的 **p5.samplerate()函数**:

    **示例:**

    ```
    var sound; 
    var spmlrt; 

    function preload() { 

        // Initialize sound 
        sound = loadSound("pfivesound.mp3"); 
    } 

    function setup() { 

        // Playing the preloaded sound 
        sound.play(); 

        //Checking loaded or not 
        var spmlrt = sound.sampleRate(); 
        console.log(spmlrt); 
    } 
    ```

    **在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
    **环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

     **支持的浏览器:****P5 . samplerate()功能**支持的浏览器如下:

    *   谷歌 Chrome
    *   微软公司出品的 web 浏览器
    *   火狐浏览器
    *   旅行队
    *   歌剧