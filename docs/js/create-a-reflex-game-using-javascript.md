# 用 JavaScript 创建一个反射游戏

> 原文:[https://www . geesforgeks . org/create-a-reflex-game-use-JavaScript/](https://www.geeksforgeeks.org/create-a-reflex-game-using-javascript/)

反射游戏是一个简单有趣的游戏，可以测量你的反应速度。制作和理解都很简单。我们将设计一个反射游戏来计算你的反应速度。规则很简单，当你看到背景颜色的变化时，只需按下停止按钮，你这样做的时间就是你的速度。
游戏提供多种颜色供你选择。一个更快的回应会比一个更慢的回应显示更好的赞美。
那么让我们从基本的 HTML 布局开始。
**HTML 布局:**
HTML 布局定义了页面的外观。这部分完全取决于你的创造力。只需记住创建一个空白的白色背景，以便变化是可见的。
其他要求的要素有:

1.  包含游戏名称和一些其他信息的标题。
2.  可以包含“从下面选择”选项的表单元素。这是必需的，以便用户可以从许多选项中选择其想要的特定颜色。
3.  两个按钮:一个用于开始游戏，另一个用于按下停止按钮。

**代码:**

```
<html>

<head>
    <title>Reflex Game</title>
</head>

<body>
    <center><strong>
      <h1 style="color: black">Reflex Game</h1>
      </strong></center>
        <center>
            <h2>Test your Response time!</h2>
        </center>
        <center>
            <h3>How To Play</h3>
            <p>Click on "Start" first, and wait until the 
              background color changes. As soon as it
              changes, hit "stop!"
            </p>

            <br>
            <form name="response">
                Change background color to:
                <select name="bgColorChange">
                    <option selected>deeppink
                        <option>aliceblue
                        <option>crimson
                        <option>darkkhaki
                        <option>cadetblue
                        <option>darkorchid
                        <option>coral
                        <option>chocolate
                        <option>mediumslateblue
                        <option>tomato
                        <option>darkslategray
                        <option>limegreen
                        <option>cornflowerblue
                        <option>darkolivegreen
                </select>
                <br>
                <br>

                <input type="button" class="btn"
                       value="Start" onClick="startit()">
                <input type="button" class="btn" 
                       value="Stop" onClick="stopTest()">
            </form>
        </center>
</body>

</html>
```

**注意:**
这是最基本的 HTML 布局。您可以在其中添加或删除任何其他部分。
**CSS 样式:**
只要有可能，你可以添加自己的自定义 CSS。在这里，我只是给按钮添加一些基本的 CSS。
**代码:**

```
<style>
  input[type=button]
{    
    background-color: #77797c;
    border: none;
    border-radius: 10%;
    color: white;
    padding: 16px 32px;
    text-decoration: none;
    margin: 4px 2px;
    cursor: pointer;
}
  </style>
```

**游戏的主要逻辑:**
游戏的主要逻辑是用 JavaScript 定义的。这里使用的 JavaScript 也非常基础，只有一点 JavaScript 知识就足以理解这一点。

我们将为这个游戏的运行制作 5 个基本功能:
**第一步:**
开始游戏。该功能需要启动按钮。一旦用户按下开始按钮，该功能将被执行。

```
function startTest()
{
    document.body.style.background=document.response.bgColorChange.options[
document.response.bgColorChange.selectedIndex].text;
    bgChangeStarted=true;
    startTime=new Date();
}
```

**第二步:**
下一个函数将是备注()函数。该功能将包括游戏结束时游戏将显示的备注。

```
function remark(responseTime)
{
    var responseString="";
    if (responseTime < 0.20)
        responseString="Well done!";
    if (responseTime >= 0.30 && responseTime < 0.20)
        responseString="Nice!";
    if (responseTime >=0.40 && responseTime < 0.30)
        responseString="Could be better...";
    if (responseTime >=0.50 && responseTime < 0.60)
        responseString="Keep practicing!";
    if (responseTime >=0.60 && responseTime < 1)
        responseString="Have you been drinking?";
    if (responseTime >=1)
        responseString="Did you fall asleep?";

    return responseString;
}
```

**第 3 步:**
按下停止按钮将执行下一个停止测试()功能。按下停止按钮可以执行 3 个选项:
第一，成功完成，告知响应时间。
其次，如果用户在按下启动按钮之前先按下停止按钮。
第三，如果用户在改变颜色之前按下停止按钮。

```
function stopTest()
{
    if(bgChangeStarted)
    {
        endTime=new Date();
        var responseTime=(endTime.getTime()-startTime.getTime())/1000;

        document.body.style.background="white";       
        alert("Your response time is: " + responseTime + 
" seconds " + "\n" + remark(responseTime));
        startPressed=false;
        bgChangeStarted=false;
    }
    else
    {
        if (!startPressed)
        {
            alert("press start first to start test");
        }
        else
        {       
            clearTimeout(timerID);
            startPressed=false;             
            alert("cheater! you pressed too early!");
        }               
    }
}
```

**第四步:**
第四个功能是获取背景变化的随机响应时间。

```
function randNumber()
{
    randSeed = (randMULTIPLIER * randSeed + randINCREMENT) % (1 << 31);
    return((randSeed >> 15) & 0x7fff) / 32767;
}
```

**最终步骤:**
最终功能是确保启动按钮没有被按下两次。

```
function startit()
{
    if(startPressed)
    {
        alert("Already started. Press stop to stop");
        return;
    }
    else
    {
        startPressed=true; 
        timerID=setTimeout('startTest()', 6000*randNumber());
    }
}
```

**最终演示和完整代码:**

```
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" 
          content="width=device-width, initial-scale=1.0">
    <meta charset="utf-8">

  <style>
  input[type=button]{    
  background-color: #77797c;
    border: none;
    border-radius: 10%;
    color: white;
    padding: 16px 32px;
    text-decoration: none;
    margin: 4px 2px;
    cursor: pointer;
}
  </style>

    <title>Reflex Game</title>
</head>
<body><script language="JavaScript">

var startTime=new Date();
var endTime=new Date();
var startPressed=false;
var bgChangeStarted=false;
var maxWait=20;
var timerID;

function startTest()
{
    document.body.style.background=document.response.bgColorChange.options[
document.response.bgColorChange.selectedIndex].text;
    bgChangeStarted=true;
    startTime=new Date();
}

function remark(responseTime)
{
    var responseString="";
    if (responseTime < 0.20)
        responseString="Well done!";
    if (responseTime >= 0.30 && responseTime < 0.20)
        responseString="Nice!";
    if (responseTime >=0.40 && responseTime < 0.30)
        responseString="Could be better...";
    if (responseTime >=0.50 && responseTime < 0.60)
        responseString="Keep practicing!";
    if (responseTime >=0.60 && responseTime < 1)
        responseString="Have you been drinking?";
    if (responseTime >=1)
        responseString="Did you fall asleep?";

    return responseString;
}

function stopTest()
{
    if(bgChangeStarted)
    {
        endTime=new Date();
        var responseTime=(endTime.getTime()-startTime.getTime())/1000;

        document.body.style.background="white";       
        alert("Your response time is: " + responseTime +
    " seconds " + "\n" + remark(responseTime));
        startPressed=false;
        bgChangeStarted=false;
    }
    else
    {
        if (!startPressed)
        {
            alert("press start first to start test");
        }
        else
        {       
            clearTimeout(timerID);
            startPressed=false;             
            alert("cheater! you pressed too early!");
        }               
    }
}

var randMULTIPLIER=0x015a4e35;
var randINCREMENT=1;
var today=new Date();
var randSeed=today.getSeconds();
function randNumber()
{
    randSeed = (randMULTIPLIER * randSeed + randINCREMENT) % (1 << 31);
    return((randSeed >> 15) & 0x7fff) / 32767;
}

function startit()
{
    if(startPressed)
    {
        alert("Already started. Press stop to stop");
        return;
    }
    else
    {
        startPressed=true; 
        timerID=setTimeout('startTest()', 6000*randNumber());
    }
}
// --> 
    </script>
        <center><strong><h1 style="color: black">Reflex Game</h1></center></strong>
        <center>
        <h2>Test your Response time!</h2>
        </center>
        <center><h3>How To Play</h3>
        <p>Click on "Start" first, and wait until the
 background color changes. As soon as it changes, hit "stop!"
        </p>

        <br>
        <form name="response">
        Change background color to: 
        <select name="bgColorChange">
        <option selected>deeppink
        <option>aliceblue
        <option>crimson
        <option>darkkhaki
        <option>cadetblue
        <option>darkorchid
        <option>coral
        <option>chocolate
        <option>mediumslateblue
        <option>tomato
        <option>darkslategray
        <option>limegreen
        <option>cornflowerblue
        <option>darkolivegreen
        </select><br>
        <br>

        <input type="button" class="btn" value="Start" onClick="startit()">
        <input type="button" class="btn" value="Stop" onClick="stopTest()">
        </form>
        </center>

    </body>
</html>
```

**输出:**

<video class="wp-video-shortcode" id="video-398913-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200414194606/My-Video21.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200414194606/My-Video21.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200414194606/My-Video21.mp4)</video>