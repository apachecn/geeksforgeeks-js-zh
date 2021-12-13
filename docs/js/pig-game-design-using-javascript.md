# 使用 JavaScript 的小猪游戏设计

> 原文:[https://www . geesforgeks . org/pig-game-design-use-JavaScript/](https://www.geeksforgeeks.org/pig-game-design-using-javascript/)

在这篇文章中，我们将解释制作著名的猪游戏所需的步骤和各种逻辑，这是一个虚拟骰子游戏。

**关于游戏:**在这个游戏中，用户界面(UI)包含了可以做三件事的用户/玩家，它们如下:

这场比赛将有两个选手。游戏开始时**玩家 1** 将是**当前层**，**玩家 2** 将是**激活的**玩家。

1.  **Roll the dice:** The current player will roll the dice, and then a random number will be generated. If the current player gets any number other than **on the dice, the number will be added to the current score ( **Initially, the current score is 0** , and then the new score will be displayed under **Current score** . **Note:** If the current player gets **1 on the dice** , the player will be switched, that is, the current player will become **active state** , and vice versa.**
2.  **hold:** If the current player clicks **hold** , then the current score will be added to **total score** . When the active player clicks the hold button, the total score of **is evaluated.** If **total score > = 100** , the current player wins; otherwise, the player is switched.
3.  **Reset:** All scores are set to 0, **Player 1** is set as the starting player (current player).

**游戏制作:**作为一款由网络浏览器渲染的游戏，它是借助 **HTML、CSS** (用于前端)和 **JavaScript** (用于后端)构建的。游戏的主要逻辑在于 JS 文件，而外观和用户界面则由 **HTML 和 CSS 渲染。**在这个项目中，基本上有四种类型的文件:

*   超文本标记语言文件(index.html)
*   文件
*   JavaScript 文件
*   图像(. png 文件索引)

我们将分析所有这些文件，从而让你了解他们在这个游戏中的工作/贡献。那么，首先让我们从**index.html**文件开始:

**超文本标记语言文件:**Index.html 文件是让网络浏览器理解并解释我们正在制作的文档类型的文件。它代表**超文本标记语言**，我们的网络浏览器通过 **V8 引擎**读取该文件并理解其组成部分(该引擎以某种语言解析代码，以便浏览器能够理解)。下面是这个游戏的 HTML 代码:

## HTML

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0" />

    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="style.css" />
    <title>Pig Game Design using JavaScript</title>
</head>

<body>
    <div class="container">
        <section class="player player--0 player--active">
            <div class="tscore">
                <h2 class="name" id="name--0">
                    Total Score<br>
                    <span class="pl">Player 1</span>
                </h2>
                <p class="score" id="score--0">43</p>
            </div>

            <div class="current">
                <p class="current-label">Current Score</p>

                <p class="current-score" id="current--0">0</p>

            </div>
        </section>

        <section class="player player--1">
            <div class="tscore">
                <h2 class="name" id="name--1">
                    Total Score<br>
                    <span class="pl">Player 2</span>
                </h2>
                <p class="score" id="score--1">24</p>
            </div>

            <div class="current">
                <p class="current-label">Current Score</p>

                <p class="current-score" id="current--1">0</p>

            </div>
        </section>

        <img src="dice-5.png" 
            alt="Playing dice" class="dice" />
        <button class="btn btn--new">Start Game</button>
        <button class="btn btn--roll">Roll dice</button>
        <button class="btn btn--hold">Hold</button>
    </div>
    <script src="gfg.js"></script>
</body>

</html>
```

在上面的代码中，我们使用了各种类(例如:BTN BTN–roll，rte)，这些类将用于 CSS 文件中的样式目的，并将在 CSS 文件下讨论它们。

**CSS 文件:**为了格式化和样式化 HTML 创建的标记，我们需要**级联样式表**，这样标记(代码)看起来会更好。下面是游戏的 CSS 代码，如下所示。在潜入代码之前，先快速看一下哪些类和 id 是为了什么目的:

1.  **For the whole HTML page and element:** * will affect every element and tag in the tag. We have used two tags to provide some specific styles, namely the styles of html and body tags.
2.  **Layout element:** The main label & **Where is the player** style? We have defined the **position** attribute for the main label and set its attribute to **relative.**
3.  **Self-made class:** The general style needed to make the page more attractive.
4.  **Absolute positioning class:** I have set the position attributes of **BTN and other classes** , and set their values to **Absolute** , because we must ensure that buttons and other elements are always in the correct position on the page. The absolute position will arrange the specific elements according to the relative positioning elements (in this case, it is the main label).

## CSS

```html
* {
    margin: 0;
    padding: 0;
}

body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container {
    position: relative;
    width: 80%;
    height: 90%;
    background-color: lightgreen;
    overflow: hidden;
    display: flex;
}

.player {
    flex: 50%;
    padding: 150px;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: all 0.75s;
}

.name {
    position: relative;
    font-weight: bold;
    font-size: 38px;
    text-align: center;
}

.pl {
    font-size: 24px;
}

.tscore {
    background-color: #fff;
    border-radius: 9px;
    width: 65%;
    padding: 2rem;
    text-align: center;
    transition: all 0.75s;
}

.score {
    font-size: 38px;
    font-weight: bold;
    margin-bottom: auto;
    padding-top: 10px;
}

.player--active {
    background-color: green;
}

.player--active .current {
    opacity: 1;
}

.current {
    margin-top: 10rem;
    background-color: #fff;
    border-radius: 9px;
    width: 65%;
    padding: 2rem;
    text-align: center;
    transition: all 0.75s;
}

.current-label {
    text-transform: uppercase;
    margin-bottom: 1rem;
    font-size: 1.7rem;
    color: #ddd;
}

.current-score {
    font-size: 3.5rem;
}

.btn {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    color: rgb(7, 124, 69);
    border: none;
    font-size: 30px;
    cursor: pointer;
    font-weight: bold;
    background-color: rgba(255, 255, 255, 0.6);
    backdrop-filter: blur(10px);
    padding: 10px 30px;
    border-radius: 10px;
}

.btn--new {
    top: 4rem;
}

.btn--roll {
    top: 39.3rem;
}

.btn--hold {
    top: 46.1rem;
}

.dice {
    position: absolute;
    left: 50%;
    top: 24rem;
    transform: translateX(-50%);
}

.player--winner {
    background-color: #003612;
}

.player--winner .name {
    font-weight: 700;
    color: #c7365f;
}

.hidden {
    display: none;
}
```

在 HTML 代码中，我们提供了各种类的名称。在这个文件中，我们提供了它们不同的功能。CSS 文件在使网页或游戏看起来很好方面起着重要的作用(仅在网络浏览器的情况下)。

到目前为止，我们已经完美地完成了游戏的用户界面，现在来了更棘手的部分。所以让我们深入**游戏逻辑……**

**JavaScript 文件:**有一些**的 JavaScript 变量，**我们可以用两种类型的变量即 **let 和常量。**可以修改用 let 声明的变量，而用常量声明的变量不能更改。在 JavaScript 文件中，我们基本上是在做 **DOM 操作**(JavaScript 中的所有东西都是一种对象，所以我们称用户界面为文档对象模型)。所以 document . queryselector()**是一种从 DOM 中选择元素的方式。**

**为了理解逻辑的工作流程，我们必须首先理解事件监听器的**概念。**事件监听器是基于特定事件执行动作的功能。他们等待特定的事件发生。本游戏共有 03 个事件监听器:**新，旧，新。**我们将了解所有这些事件监听器的功能:**

****注意:**在前往事件处理程序部分之前，我们必须在文件中声明一些变量，以便稍后在我们的游戏逻辑中使用它们。**

## **Javascript**

```html
'use strict';

// Selecting elements
const player0El = document.querySelector('.player--0');
const player1El = document.querySelector('.player--1');
const score0El = document.querySelector('#score--0');
const score1El = document.getElementById('score--1');
const current0El = document.getElementById('current--0');
const current1El = document.getElementById('current--1');

const diceEl = document.querySelector('.dice');
const btnNew = document.querySelector('.btn--new');
const btnRoll = document.querySelector('.btn--roll');
const btnHold = document.querySelector('.btn--hold');

let scores, currentScore, activePlayer, playing;
```

**在 JavaScript 文件的最开始，有一行“使用严格”。“使用严格”的目的是表明代码应该以“严格模式”执行。除了 Internet Explorer 9 及更低版本，所有现代浏览器都支持“使用严格”。**

**现在让我们开始查看 3 个事件处理程序的代码。**

****1。****

## **Javascript**

```html
// Rolling dice functionality
btnRoll.addEventListener('click', function () {
  if (playing) {

    // 1\. Generating a random dice roll
    const dice = Math.trunc(Math.random() * 6) + 1;

    // 2\. Display dice
    diceEl.classList.remove('hidden');
    diceEl.src = `dice-${dice}.png`;

    // 3\. Check for rolled 1
    if (dice !== 1) {

      // Add dice to current score
      currentScore += dice;
      document.getElementById(
        `current--${activePlayer}`
      ).textContent = currentScore;
    } else {

      // Switch to next player
      switchPlayer();
    }
  }
});
```

**每当玩家点击**滚动按钮**时，该事件处理程序就会运行(这就是为什么我们在那里使用了点击事件)。然后有一个回调函数，以一个 **if-else 块**开始。因为我们已经声明了变量 **playing = true** ，所以这个事件处理程序的 if 块将为 true，因此 if 块的代码将被执行。下面是前面的步骤:**

***   **Step 1:** After the player clicks the dice button, this event handler uses the **math.trunc () function to generate a random number.** We use the Math.trunc () function because it returns the integer part of the randomly generated function and adds 1 to it, because **random () function** can generate any number from 0 to 1, but in our example, we only need numbers from 1 to 6\. < br > **Understanding dice variables:** Dice variables will store randomly generated numbers. Suppose the Math.random () function generates the **number 0.02\.** According to the code, the first 0.02 will be multiplied by 6\. So the value of the variable dice is now 0.12\. Then the Math.trunc () function will start to run, and make the **dice variable 0** . 1 will now be added to the variable, which will make **dice = 1** (this is the number that our dice need).*   **Step 2:** Now that we have got the score of the dice, we must display the dice corresponding to the number of dice. (In the CSS file, we made a class named hidden, which will make the dice be hidden at the beginning of the game.) But now that we have a dice number to be displayed in the form of dice image, we must delete the **hidden class.** This is achieved by the line **dice 1.classlist.remove ('hide')** , and then the correct image of dice is rendered to the user interface.*   **Step3。** Now, according to the rules of the game, we have to check the numbers on the dice. Therefore, if the number of dice is not 1, **the current score is updated** . If the number of dice is 1, call **to switch the player ()** .**

## **Javascript**

```html
const switchPlayer = function () {
  document.getElementById(`current--${activePlayer}`).textContent = 0;
  currentScore = 0;
  activePlayer = activePlayer === 0 ? 1 : 0;
  player0El.classList.toggle('player--active');
  player1El.classList.toggle('player--active');
};
```