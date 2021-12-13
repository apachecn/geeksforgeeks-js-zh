# 如何使用 JavaScript 创建水平和垂直选项卡？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 创建水平和垂直选项卡/](https://www.geeksforgeeks.org/how-to-create-horizontal-and-vertical-tabs-using-javascript/)

选项卡可用于以有组织的方式在单个页面上显示大量内容。我们可以使用 HTML、CSS 和 JavaScript 设计单页标签。HTML 元素用于设计选项卡的结构以及段落中的内容。样式是使用 CSS 执行的。单击每个选项卡按钮，选项卡会显示各自的内容。这是使用 JavaScript 完成的。

**水平制表符:**下面的代码演示了带有制表符的简单 HTML 结构及其段落形式的内容。单击每个选项卡，它调用在下面给出的“script.js”文件中实现的 *displayContent()* 方法。

**HTML 代码:**

## HTML

```html
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
</head>

<body>
    <h2 style="color:green">
        GeeksforGeeks Horizontal tabs
    </h2>

    <!-- Link to each tab with onclick event -->
    <div id="tabsDiv">
        <button class="linkClass" onclick=
            "displayContent(event, 'interview')">
            Interview
        </button>

        <button class="linkClass" onclick=
            "displayContent(event, 'practice')">
            Practice
        </button>

        <button class="linkClass" onclick=
            "displayContent(event, 'python')">
            Python
        </button>

        <button class="linkClass" onclick=
            "displayContent(event, 'algorithms')">
            Algorithms
        </button>

        <button class="linkClass" onclick=
            "displayContent(event, 'machine')">
            Machine Learning
        </button>
    </div>

    <!-- Content for each HTML tab  -->
    <div id="interview" class="contentClass">
        <h3>Interview</h3>

        <p>
            Also, in Asymptotic analysis, we always
            talk about input sizes larger than a
            constant value. It might be possible
            that those large inputs are never given
            to your software and an algorithm which is
            asymptotically slower, always performs
            better for your particular situation.
            So, you may end up choosing an algorithm
            that is Asymptotically slower but faster
            for your software.
        </p>

    </div>

    <div id="practice" class="contentClass">
        <h3>Practice</h3>

        <p>
            Asymptotic Analysis is the big idea
            that handles above issues in analyzing
            algorithms. In Asymptotic Analysis,
            we evaluate the performance of an 
            algorithm in terms of input size (we 
            don’t measure the actual running time).
            We calculate, how does the time
            (or space) taken by an algorithm
            increases with the input size.
        </p>

    </div>

    <div id="python" class="contentClass">
        <h3>Python</h3>

        <p>
            Python is a high-level, general-purpose
            and a very popular programming language.
            Python programming language (latest Python 3)
            is being used in web development, Machine
            Learning applications, along with all
            cutting edge technology in Software Industry.
            Python Programming Language is very well
            suited for Beginners, also for experienced
            programmers with other programming languages
            like C++ and Java.
        </p>
    </div>

    <div id="algorithms" class="contentClass">
        <h3>Greedy Algorithms</h3>

        <p>
            Greedy is an algorithmic paradigm that
            builds up a solution piece by piece,
            always choosing the next piece that
            offers the most obvious and immediate
            benefit. So the problems where
            choosing locally optimal also
            leads to global solution are
            best fit for Greedy.
        </p>
    </div>

    <div id="machine" class="contentClass">
        <h3>Machine Learning</h3>

        <p>
            Machine Learning is the field of
            study that gives computers the capability
            to learn without being explicitly
            programmed. ML is one of the most
            exciting technologies that one
            would have ever come across.
            As it is evident from the name,
            it gives the computer that makes
            it more similar to humans:
            The ability to learn. Machine learning
            is actively being used today,
            perhaps in many more places than
            one would expect.
        </p>
    </div>
</body>

</html>
```