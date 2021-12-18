# p5.js | loadSound()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-loadsound-function/](https://www.geeksforgeeks.org/p5-js-loadsound-function/)

**p5.loadSound** 是 p5.sound 库的一个内置函数，包含将作为网络音频播放的对象的路径。您可以轻松附加任何支持客户端浏览器的文件。所以要谨慎选择，更好的是制作一个文件格式的数组，当客户端的浏览器支持这种格式时就会导入。像 **mp3** 、 **ogg** 、 **wav** 等。

**语法:**

```
p5.loadSound(path, [successCallback], [errorCallback], [whileLoadingCallback])
```

**参数:**该功能接受四个参数，如上所述，描述如下:

*   **路径:**此参数将文件的路径保存为字符串，可以添加多个文件。
*   **成功回调:**该参数保存文件加载时的函数，是可选参数。
*   **errorCallback:** 如果前一个参数想要调用的函数失败，这个参数保存错误的函数。如果可执行的函数不能被调用，这个参数将处理这个问题，并告知出了什么问题。它也是一个可选参数。
*   **whileLoadingCallback:** 该参数保存页面加载时要调用的函数，也是可选的。

下面的例子说明了 JavaScript 中的 **p5.loadSound()函数**:

**示例:**

```
var sound;

function preload() {

    // Initialize sound
    sound = loadSound("pfivesound.mp3");
}

function setup() {

    // Playing the preloaded sound
    sound.play();
} 
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**浏览器支持 **p5.loadSound** 功能如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧