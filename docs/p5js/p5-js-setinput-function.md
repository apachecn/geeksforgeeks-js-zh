# p5.js | setInput()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-setinput-function/](https://www.geeksforgeeks.org/p5-js-setinput-function/)

**setInput()函数**是 p5.js 库中的一个内置函数。该函数用于连接默认情况下作为主输出的 p5sound 实例。通过使用这个函数，您还可以传入一个特定的源。

**语法:**

```
setInput(snd, smoothing)
```

**注意:**所有与声音相关的功能只有当声音库包含在**index.html**文件的头段中时才起作用。

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **snd:** 此参数用于设置声源，可选。
*   **平滑:**此参数用于设置平滑幅度读数，范围在 0.0 到 1.0 之间，此参数也是可选的。

下面的例子说明了 JavaScript 中的 **p5.setInput()函数**:

```
function preload(){
  sound1 = loadSound('song.mp3');
  sound2 = loadSound('pfivesound.mp3');
}
function setup(){
  amplitude = new p5.Amplitude();
  sound1.play();
  sound2.play();
  amplitude.setInput(sound2);
}
function draw() {
  background(255);
  fill(200);
  let gfg = amplitude.getLevel();
  let size = map(gfg, 0, 1, 0, 400);
  ellipse(width/1, height/1, size*2, size*2);
}
function mousePressed(){
  sound2.pause();
}

function mouseReleased(){
  sound2.play();
}
```

**在线编辑:**[【https://editor.p5js.org/】](https://editor.p5js.org/)
**环境设置:**[https://www . geeksforgeeks . org/P5-js-soundfile-object-installation-and-methods/](https://www.geeksforgeeks.org/p5-js-soundfile-object-installation-and-methods/)

**支持的浏览器:**T2 P5 . js setInput()功能支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   旅行队
*   歌剧