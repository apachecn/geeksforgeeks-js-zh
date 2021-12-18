# 用 JavaScript 设计一款打字速度测试游戏

> 原文:[https://www . geesforgeks . org/design-a-打字-速度-测试-游戏-使用-javascript/](https://www.geeksforgeeks.org/design-a-typing-speed-test-game-using-javascript/)

打字测试旨在找出一个人在给定时间内打字的速度。我们将使用 JavaScript 设计一个打字游戏，该游戏提出了一个简单的打字挑战，并通过计算每分钟字符数(CPM)、每分钟单词数(WPM)和打字字符的准确性来发现打字的性能。
游戏显示了一系列必须在指定时限内输入的报价，速度越快越好。更高的打字速度将显示更高的 WPM 值。键入错误的字符将在键入过程中被相应地标记。
我们先创建 HTML 布局，用 CSS 样式化，然后用 JavaScript 编写逻辑。
**HTML 布局:**HTML 布局定义了将在页面上显示的元素结构。这包括:

*   **表头部分:**此部分显示当前打字会话的统计数据。这包括显示剩余时间、错误数量、准确性、WPM 和 CPM。
*   **引用部分:**该部分显示了必须在输入区键入的当前文本。
*   **输入区域:**该部分包含需要输入文本的输入区域。
*   **重启按钮:**这是重启按钮，一旦时间用完，游戏结束，就会显示。
*   **代码:**

## 超文本标记语言

```
<html lang="en">
<head>
    <title>Simple Speed Typer</title>

    <!-- link the CSS file here -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <div class="heading">
      Simple Speed Typing
    </div>
    <div class="header">
      <div class="wpm">
        <div class="header_text">WPM</div>
        <div class="curr_wpm">100</div>
      </div>
      <div class="cpm">
        <div class="header_text">CPM</div>
        <div class="curr_cpm">100</div>
      </div>
      <div class="errors">
        <div class="header_text">Errors</div>
        <div class="curr_errors">0</div>
      </div>
      <div class="timer">
        <div class="header_text">Time</div>
        <div class="curr_time">60s</div>
      </div>
      <div class="accuracy">
        <div class="header_text">% Accuracy</div>
        <div class="curr_accuracy">100</div>
      </div>
    </div>

    <div class="quote">
      Click on the area below to start the game.
    </div>
    <textarea class="input_area"
      placeholder="start typing here..."
      oninput="processCurrentText()"
      onfocus="startGame()">
    </textarea>
    <button class="restart_btn"
      onclick="resetValues()">
      Restart
    </button>
  </div>

  <!-- link the JavaScript file here -->
  <script src="game.js">
  </script>
</body>
</html>
```

**注意:**每个部分都填充了虚拟数据，使造型更容易。上面的 HTML 代码如下。
**CSS 样式:** CSS 用于设置不同部分的样式，使其更具视觉吸引力。

*   标题部分使用 flex 布局显示。
*   每个元素都有足够的填充和边距。
*   每个元素的文本大小使得用户在玩游戏时容易阅读。
*   定义了两个额外的类来表示正确或错误键入的字母。这些类将在需要时动态添加或删除。
*   **代码:**

## 超文本标记语言

```
body {
  background-color: #fe9801;
  color: black;
  text-align: center;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.heading {
  margin-bottom: 20px;
  font-size: 3rem;
  color: black;
}

.header {
  display: flex;
  align-items: center;
}

.timer, .errors, .accuracy,
.cpm, .wpm {
  background-color: #ccda46;
  height: 60px;
  width: 70px;
  margin: 8px;
  padding: 12px;
  border-radius: 20%;
  box-shadow: black 5px 8px 5px;
}

.cpm, .wpm  {
  display: none;
}

.header_text {
  text-transform: uppercase;
  font-size: 0.6rem;
  font-weight: 600;
}

.curr_time, .curr_errors,
.curr_accuracy, .curr_cpm,
.curr_wpm {
  font-size: 2.75rem;
}

.quote {
  background-color: #ccda46;
  font-size: 1.5rem;
  margin: 10px;
  padding: 25px;
  box-shadow: black 5px 8px 5px;
}

.input_area {
  background-color: #f5f5c6;
  height: 80px;
  width: 40%;
  font-size: 1.5rem;
  font-weight: 600;
  margin: 15px;
  padding: 20px;
  border: 0px;
  box-shadow: black 5px 8px 5px;
}

.restart_btn {
  display: none;
  background-color: #326765;
  font-size: 1.5rem;
  padding: 10px;
  border: 0px;
  box-shadow: black 5px 8px 5px;
}

.incorrect_char {
  color: red;
  text-decoration: underline;
}

.correct_char {
  color: darkgreen;
}
```