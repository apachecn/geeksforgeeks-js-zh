# p5.js | randomSeed()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-randomseed-function/](https://www.geeksforgeeks.org/p5-js-randomseed-function/)

p5.js 中的 **randomSeed()函数**用于每次运行程序时返回一个随机数。 **random()** 和 **randomSeed()** 函数的区别在于，random()函数在每次运行程序时都会产生不同的值，但是当使用 randomSeed()函数时，它会在每次运行程序时给出一个恒定的随机数。

**语法:**

```
randomSeed( Seed )
```

**参数:**此功能接受单参数**种子**，任意整数值。

**返回值:**返回一个常量随机数。

下面的程序说明了 p5.js 中的 randomSeed()函数:

**示例 1:** 本示例使用 randomSeed()函数在每次运行程序时返回一个随机数。

```
function setup() { 

    // Creating Canvas size
    createCanvas(550, 140); 

    // Set the background color 
    background(220); 

    // Calling to randomSeed() function
    randomSeed(9)

    // Calling to random() function with
    // min and max parameters
    let A = random(1, 2);
    let B = random(0, 1);
    let C = random(2);
    let D = random(2, 10);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting random number
    text("Random number between 1 and 2 is: " + A, 50, 30);
    text("Random number between 0 and 1 is: " + B, 50, 60);
    text("Random number between 0 and 2 is: " + C, 50, 90);
    text("Random number between 2 and 10 is: " + D, 50, 110);
} 
```

**输出:**
![](img/e97e8d3f237ae1fd17984de52ac2eac7.png)

**注意:**在上面的例子中，在变量“C”中只传递了一个参数，然后它返回一个从下限 0 到上限的随机数。

**示例 2:** 本示例使用 randomSeed()函数在每次运行程序时返回一个随机数。

```
function setup() { 

    // Creating Canvas size
    createCanvas(550, 140); 

    // Set the background color 
    background(220); 

    // Calling to randomSeed() function
    randomSeed(9)

    // Calling to random() function with
    // parameter array of some elements
    let A = random([1, 2, 3, 4]);
    let B = random([0, 1]);
    let C = random([2, 6, 7, 9]);
    let D = random([2, 10]);

    // Set the size of text 
    textSize(16); 

    // Set the text color 
    fill(color('red')); 

    // Getting random number
    text("Random number is: " + A, 50, 30);
    text("Random number is: " + B, 50, 60);
    text("Random number is: " + C, 50, 90);
    text("Random number is: " + D, 50, 110);
}    
```

**输出:**
![](img/54f23b71c3ae7bd8eb8f8ca10c04c0b3.png)

**参考:**T2】https://p5js.org/reference/#/p5/randomSeed