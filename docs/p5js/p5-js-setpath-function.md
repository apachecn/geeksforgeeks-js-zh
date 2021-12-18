# p5.js | setPath()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-setpath-function/](https://www.geeksforgeeks.org/p5-js-setpath-function/)

**setPath()函数**是 p5.js 库中的一个内置函数。此功能用于重置新路径的声音文件的来源。

**语法:**

```
setPath(path, callback)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **路径:**此参数保存新文件的路径。
*   **回调:**此参数是将要调用的函数的名称。

下面的例子说明了 JavaScript 中的 **p5.setPath()函数**:

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3");
    sounds = loadSound("pfivesounds.mp3") 
} 

function setup() { 

    // Playing the preloaded sound 
    sound.play();
    //sound will play twice fast 
    sound.setpath(sounds/pfivesound.mp3, gfg);
} 
 function gfg() {
    alert("setPath function called successfully")
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