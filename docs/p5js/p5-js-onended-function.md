# p5.js | onended()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-onended-function/](https://www.geeksforgeeks.org/p5-js-onended-function/)

**onended()函数**是 p5.js 库中的一个内置函数。此功能用于在声音文件到达结尾时安排一个事件，这意味着如果您正在播放音频，您可以安排该音频到达其持续时间结尾时的任何事件。使用带有此功能的循环时要小心，否则计划的事件将不会触发。

```
onended(callback)
```

 **注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **回调:**此参数是音频到达缓冲区末尾时将调用的函数的名称。

以下示例说明了 JavaScript 中的 **p5.onended()函数**:
**示例 1:** 在本例中，音频将无循环播放。

```
var sound;

function setup() {

    // Initialize sound 
    sound = createAudio('pfivesound.mp3');

    // Playing the sound 
    sound.play();

    // event define after end of audio
    sound.onended(geeks);

  }

  //event that will occur 
  function geeks(dur) {
    alert('Audio ended ');
  }

```

**输出:**音频结束后。
T3】

**示例 2:** 在此示例中，音频将以循环播放。所以不会有什么大事。

```
var sound;

function setup() {

     // Initialize sound 
    sound = createAudio('pfivesound.mp3');

    // Playing the sound 
    sound.play();

    // looping the sound 
    sound.loop();

    // event define after end of audio
    sound.onended(geeks);
  }

  function geeks(dur) {
    alert('Audio ended ');
  }

```

**输出:**

```
No event will occur
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**功能 **p5.js onended()** 支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧