# P5 . js | clear clues()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-clearcues-function/](https://www.geeksforgeeks.org/p5-js-clearcues-function/)

**ClearKeys()函数**是 p5.js 库中的一个内置函数。该函数用于删除 addCue()函数指定的所有任务。

**语法:**

```
clearCues()
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**本功能不接受任何参数:

以下示例说明了 JavaScript 中的 p5.clearCue()函数:
**示例:**

```
var sound;

function setup() {

    // Initialize sound 
    sound = createAudio('song.mp3');

    // Playing the sound 
    sound.play();

    // event define after end of audio
    sound.addCue(5, geeks);
    sound.addCue(10, pse);

    // clearing all the addCue event
    sound.clearCues();
  }

  //event that will occur in 5 sec
  function geeks(dur) {
    alert('addCue function running');
  }

  //event that will occur in 10 sec
  function pse() {
    sound.pause();
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