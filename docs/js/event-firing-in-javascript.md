# JavaScript 中的事件触发

> 原文:[https://www.geeksforgeeks.org/event-firing-in-javascript/](https://www.geeksforgeeks.org/event-firing-in-javascript/)

### 什么是事件？

事件是发生在我们进行编程的系统中的动作或事件，系统会告诉您这些动作或事件，以便我们可以根据需要以某种方式响应这些事件。例如，如果用户在网页上选择了一个按钮，可能需要通过显示一个对话框来响应该操作。

### 了解事件的基本知识:

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<body>
    <button class="first">Button 1</button>
    <button class="second">Button 2</button>
    <button class="third">Button 3</button>

    <script>
        const firstBtn = document.querySelector(".first");
        const secondBtn = document.querySelector(".second");
        const thirdBtn = document.querySelector(".third");

        firstBtn.addEventListener('click', ()=>{
            console.log("Button 1 is Clicked");
        });
        secondBtn.addEventListener('click', ()=>{
            console.log("Button 2 is Clicked");
        });

        thirdBtn.addEventListener('click', ()=>{
            console.log("Button 3 is Clicked");
        });

    </script>
</body>

</html>
```

**输出:**

```html
Button 1 is Clicked
Button 2 is Clicked
Button 3 is Clicked
```

当按钮 1 被点击时，我们在控制台中得到的输出是**按钮 1 被点击**并且类似地取决于被点击的按钮。这里我们有一个事件处理程序，它与查找点击事件的按钮相关联。

在 JavaScript 中，我们有一个事件对象，它包含与该事件相关的所有信息，这些信息可以用来找出哪个事件正在被激发。考虑上面的例子，现在我们进行以下修改。

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<body>
    <button class="first">Button 1</button>
    <button class="second">Button 2</button>
    <button class="third">Button 3</button>

    <script>
        const firstBtn = document.querySelector(".first");
        const secondBtn = document.querySelector(".second");
        const thirdBtn = document.querySelector(".third");

        firstBtn.addEventListener('click', (e)=>{
            console.log(e.target);
        });

        secondBtn.addEventListener('click', (e)=>{
            console.log(e.target);
        });

        thirdBtn.addEventListener('click', (e)=>{
            console.log(e.target);
        });
    </script>
</body>
</html>
```

**输出:**

```html
Button 1
Button 2
Button 3
```

我们已经将事件对象作为参数传递给了函数，该函数将在事件被激发时执行。目标属性告诉我们触发事件的元素，因此我们得到了我们想要的答案。这就是我们如何在 JavaScript 中使用事件对象来知道哪个元素被激发或者什么类型的元素被激发。

如果我们将 *e.target* 替换为仅仅 *e* ，我们将得到事件对象作为输出，可以用来提取关于事件的任何信息。

## 超文本标记语言

```html
<!DOCTYPE html>
<html lang="en">

<body>
    <button class="first">Button 1</button>
    <button class="second">Button 2</button>
    <button class="third">Button 3</button>

    <script>
        const firstBtn = document.querySelector(".first");
        const secondBtn = document.querySelector(".second");
        const thirdBtn = document.querySelector(".third");

        firstBtn.addEventListener('click', (e)=>{
            console.log(e.type);
        });

        secondBtn.addEventListener('click', (e)=>{
            console.log(e.type);
        });

        thirdBtn.addEventListener('click', (e)=>{
            console.log(e.type);
        });
    </script>
</body>

</html>
```

**输出:**

```html
click
click
click
```