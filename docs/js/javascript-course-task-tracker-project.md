# JavaScript 课程|任务跟踪器项目

> 原文:[https://www . geesforgeks . org/JavaScript-课程-任务-跟踪器-项目/](https://www.geeksforgeeks.org/javascript-course-task-tracker-project/)

**上一篇:** [JavaScript 课程| JavaScript 中的对象](https://www.geeksforgeeks.org/javascript-course-objects-in-javascript/)
**项目介绍**
在本课程的最后一篇文章中，我们将学习如何制作一个简单的 JavaScript 应用程序，在这里我们可以添加任务、删除任务以及编辑任务。纯(香草)JavaScript 已经被使用，我们也将大量使用 DOM 操作，所以主要的先决条件之一是 [HTML | DOM](https://www.geeksforgeeks.org/dom-document-object-model/) 。

**项目结构**

> **index . html**
> **styles . CSS****list . js**

*   **index.html**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <title>Task Tracker</title>
  <link rel="stylesheet" href="styles.css" type="text/css"
    media="screen" charset="utf-8">
</head>

<body>
  <div class="container">

<p>
      <label for="new-task" class="middle">Add Task</label>
    <input id="new-task" type="text"><button>Add Task</button>
    </p>

    <h3 class="middle">Todo</h3>
    <ul id="incomplete-tasks">
    </ul>

    <h3 class="middle">Completed Tasks</h3>
    <ul id="completed-tasks">
    </ul>
  </div>

  <script type="text/javascript" src="list.js"></script>

</body>

</html>
```