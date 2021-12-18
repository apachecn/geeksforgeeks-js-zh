# p5.js |暂停()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-pause-function/](https://www.geeksforgeeks.org/p5-js-pause-function/)

**pause()函数**是 p5.js 库中的一个内置函数。此功能用于暂停网络上播放的音频。暂停函数应该在 play()函数之后调用。如果你在那之前打电话，它没有什么可暂停的。

**语法:**

```
pause( startTime )
```

**注意:**所有与声音相关的功能只有当声音库包含在 index.html 文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **开始时间:**该参数以秒为单位保存定义计划事件的整数，是可选参数。

下面给出的示例说明了 JavaScript 中的 **p5.js pause()函数**:
**示例:**

```
var sound; 

function preload() { 

    // Initialize sound 
    sound = loadSound("song.mp3"); 
} 

function setup() {
    sound.loop();
  }
  function keyTyped() {
    if (key == 'g') {
        sound.pause();
    }
  }

  function keyReleased() {
    if (key == 'g') {
        sound.play();
    }
  }
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . js pause()功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧