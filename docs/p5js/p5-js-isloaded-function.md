# p5.js | isLoaded()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-isloaded-function/](https://www.geeksforgeeks.org/p5-js-isloaded-function/)

**是 Loaded()函数**是 p5.sound 库的一个内置函数，用于验证 **loadSound()** 函数是否成功执行，如果 loadSound 成功，则该函数将返回 true，否则返回 false。这意味着它返回布尔值。

**语法:**

```
isLoaded()
```

**注意:**所有与声音相关的功能只有当声音库包含在 index.html 文件的头段中时才起作用。

**参数:**此功能不接受任何参数。

下面的例子说明了 JavaScript 中的 **p5.isLoaded()函数**:
**例子:**

```
var sound; 
var load;

function preload() { 

    // Initialize sound 
    sound = loadSound("pfivesound.mp3"); 
} 

function setup() { 

    //Checking loaded or not
    var load = sound.isLoaded();
    console.log(load);

    // Playing the preloaded sound 
    sound.play(); 
} 
```

**输出:**

```
true
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:****P5 . is loaded 功能**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧