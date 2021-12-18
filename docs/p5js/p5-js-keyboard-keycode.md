# p5.js |键盘键码

> 原文:[https://www.geeksforgeeks.org/p5-js-keyboard-keycode/](https://www.geeksforgeeks.org/p5-js-keyboard-keycode/)

p5.js 中的**键码**变量始终包含最近按下的按键的键码。建议在确定用户是否按下了修饰键(如 Shift、Control、大写锁定键或功能键)时使用该键码。

**语法:**

```
keyCode
```

下面的程序举例说明了 p5.js 中的**键码**变量:
**示例:**

## java 描述语言

```
function setup() {
  createCanvas(400, 300);
}

function draw() {
  clear();
  textSize(18);
  fill("black");
  text("Press any key to see its keyCode", 60, 20);
  text("The name of the key pressed", 70, 60);

  textSize(52);
  fill("red");

  // Show the key that is recently pressed
  text(key, 170, 120);
  textSize(18);
  fill("black");

  text("The keyCode of the key pressed", 60, 160);
  textSize(52);
  fill("red");

  // Show the key code of the key that is
  // recently pressed
  text(keyCode, 160, 220);
}
```