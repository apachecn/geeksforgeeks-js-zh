# 如何用纯 JavaScript 添加淡出效果？

> 原文:[https://www . geesforgeks . org/如何使用纯 javascript 添加淡入淡出效果/](https://www.geeksforgeeks.org/how-to-add-fade-out-effect-using-pure-javascript/)

淡入淡出效果被描述为所选部分不透明度的逐渐增加和减少。换句话说，褪色效应被称为不透明度随时间的增加和减少。当应用这种效果时，不透明度逐渐降低，这就是所谓的淡出效果。这是用于以选定的时间间隔淡出页面上选定部分的效果。淡出和淡入效果在网络项目中使用非常好，因为它强调了网页的样式。

淡出效果用于将选定元素的不透明度从可见更改为隐藏。通过使用此方法，淡入淡出的元素将不会占用任何空间。我们在这个逻辑中使用了 setInterval 方法和 clearInterval 方法。

**代码中使用的内置函数语法:**

*   **设定区间():**取两个参数为:

    ```
    setInterval(function_reference, time interval)
    ```

*   **clearInterval():** 取单参数为:

    ```
    clearInterval(parameterof time to stop calling a function)
    ```

**方法 1:** 在页面加载时，我们正在调用一个名为 fadeout()的函数，其中我们使用了 setInterval()方法，该方法采用了两个参数:一个是函数引用(在本例中是隐藏的)，另一个是 timer(以数字表示)。
在隐藏函数中，我们将属性不透明度放在名为不透明度的变量中，并在每次调用淡出函数时将其减少 0.1。

**例 1:**

```
<html>
<head>
    <title>How to create fade-out effect 
            on page load using javascript</title>
    <script type="text/javascript">

    var opacity=0;
    var intervalID=0;
    window.onload=fadeout;
        function fadeout(){
               setInterval(hide, 200);
        }
    function hide(){
          var body=document.getElementById("body");
          opacity =
 Number(window.getComputedStyle(body).getPropertyValue("opacity"))

            if(opacity>0){
                   opacity=opacity-0.1;
                           body.style.opacity=opacity
            }
            else{
                clearInterval(intervalID); 
            }
        } 
    </script> 

</head>

<body id="body">

<br>

    <h1 style="color: green"> 
        GeeksForGeeks 
    </h1> 

    <b> 
        How to create fade-out effect 
        on page load using javascript 
    </b>

    <p> 
        This page will fade-out 
        after loading 
    </p> 
</body>
</html>    
```

**输出:**

<video class="wp-video-shortcode" id="video-399953-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200417164903/output-of-fade-out-effect-using-pure-javascript.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200417164903/output-of-fade-out-effect-using-pure-javascript.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200417164903/output-of-fade-out-effect-using-pure-javascript.mp4)</video>

**说明:**

**注意:**不透明度介于 0-1 之间，在这种情况下，初始不透明度值取 1。

*   在上述代码中，淡出效果的部分由`id(body in this case)`选择。
*   **window.onload=fadeout** ，用于页面继续加载时自动调用 fadeout()功能。
*   在 fadeout()函数中，还调用了一个名为 setInterval()的函数，该函数每隔 200 毫秒调用一次 hide()函数，直到调用 clearInterval()为止，当选定部分的不透明度为零时，将调用 clearInterval()。
*   在 hide function 中，编写了简单的逻辑，用于在每次对选定零件调用 fadeout()函数时将不透明度降低 0.1。在本例中， **getPropertyValue(“不透明度”)**，用于选择属性不透明度。
*   这些工作一直持续到不透明度变为 0。

**方法-2:** 在这种方法中，完整的逻辑写在变量内部，这是借助 setInterval()方法完成的，这里要写完整的函数来代替函数引用。这种方法相对容易。

**例 2:**

```
<html>
<head>
    <title>How to create fade-out effect 
            on page load using javascript</title>
  <script type="text/javascript">

         window.onload=fadeout;

         function fadeout() {
    var fade= document.getElementById("body");

    var intervalID = setInterval(function () {

        if (!fade.style.opacity) {
            fade.style.opacity = 1;
        }

        if (fade.style.opacity > 0) {
            fade.style.opacity -= 0.1;
        } 

        else {
            clearInterval(intervalID);
        }

    }, 200);
}

     </script> 
    </head>
<body id="body">
<br>

    <h1 style="color: green"> 
        GeeksForGeeks 
    </h1> 

    <b> 
        How to create fade-out effect 
        on page load using javascript 
    </b>

    <p> 
        This page will fade-out after loading 
    </p> 
</body>
</html>
```

**输出:**

<video class="wp-video-shortcode" id="video-399953-2" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200419155825/output-of-fade-out-effect-using-pure-javascript1.mp4?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20200419155825/output-of-fade-out-effect-using-pure-javascript1.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200419155825/output-of-fade-out-effect-using-pure-javascript1.mp4)</video>

**说明:**

**注意:**不透明度介于 0-1 之间，在这种情况下，初始不透明度值设置为 1。

*   在上述代码中，淡出效果的部分由`id(body in this case).`选择
*   **window.onload=fadeout** ，用于页面加载时自动调用 fadeout()功能。
*   在 fadeout()函数中，我们在调用 setInterval()方法的 intervalId 变量中定义我们的逻辑，这里不是给出函数引用，而是定义整个函数。
*   在 defined function 中，每次我们将 style.opacity 与 0 进行比较时，如果大于 0，就会执行一个操作，将不透明度降低 0.1，当该值变为 0 时，就会自动调用 clear function。
*   这个过程一直持续到不透明度变为 0，并且调用了 clear 函数。

我们取了 0.1 和 200 毫秒作为数值，任何数值都是可以接受的。