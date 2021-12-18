# p5.js | removeCue()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-removecue-function/](https://www.geeksforgeeks.org/p5-js-removecue-function/)

**removeCue()函数**是 p5.js 库中的一个内置函数。此函数用于移除由 addCue()函数指定的任务。该任务将被选为 addCue()函数给出的 id。这里 id 是提示的索引号 0 表示第一个事件，1 表示第二个事件，依此类推。

**语法:**

```
removeCue(id)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **id:** 此参数保存一个整数，该整数定义了由 addCue()函数返回的提示的 id

下面的例子说明了 JavaScript 中的 p5.remove()函数:

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

    // removing the 1st addCue event
    sound.removeCue(0);
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