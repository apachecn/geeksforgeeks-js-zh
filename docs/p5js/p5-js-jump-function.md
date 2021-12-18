# p5.js | jump()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-jump-function/](https://www.geeksforgeeks.org/p5-js-jump-function/)

**跳转()函数**是 p5.js 库中的一个内置函数。该功能用于在播放音频的某个特定点跳转，只需要该音频的时间位置即可。在网上播放这段时间。

**语法:**

```
jump( cueTime, duration )
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受两个参数，如上所述，如下所述。

*   **cueTime:** 此参数以秒为单位保存一个整数，以秒为单位定义提示时间。
*   **持续时间:**此参数保存一个整数，以秒为单位定义播放持续时间。

下面的例子说明了 JavaScript 中的 **p5.js jump()函数**:

**示例 1:** 在此示例中，歌曲将在歌曲的第二个 7 位置跳转。

## java 描述语言

```
var sound;

function preload() {

    // Initialize sound
    sound = loadSound("pfivesound.mp3");
}

function setup() {

    // Playing the preloaded sound
    sound.play();
    //sound will jump at that point
    sound.jump( 7 );

}
```

**例 2:** 在本例中，如果按下按钮，歌曲将在歌曲的中间位置跳转。

## java 描述语言

```
var sound;
var jmp;  

function preload() {

    // Initialize sound
    sound = loadSound("song.mp3");
}

function setup() {

    // Playing the preloaded sound
    sound.play();

    //Creating button
    jmp = createButton("Jump");
    jmp.mousePressed(jumpAudio);
}

function jumpAudio() {

    //sound will jump at that point
    var len = sound.duration();
    sound.jump( len/2);
}
```

**注意:**过了中间位置后可能再按一次按钮，会从中间位置播放另一首时间歌曲。

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js 跳转()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧