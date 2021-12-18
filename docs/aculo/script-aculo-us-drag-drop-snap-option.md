# 拖动&放置捕捉选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-拖放-snap-option/](https://www.geeksforgeeks.org/script-aculo-us-drag-drop-snap-option/)

脚本中的**捕捉**选项**拖放**模块用于将可拖动元素捕捉到网格或限制其在定义空间中的移动。默认情况下，它设置为 false。它可以用单个值或函数来定义，该函数将定义元素将捕捉的位置。

**语法:**

```
new Draggable ('element_id', {snap: size of the snap});
```

**值:**

*   **捕捉:**用于使可拖动元素约束其运动。

**示例:**

## 超文本标记语言

```
<html>
<head>
  <script type="text/javascript" 
          src="prototype.js">
  </script>
  <script type="text/javascript" 
          src="scriptaculous.js">
  </script>
  <script>
    var elements = ['element'];
    window.onload = function () {
      elements.each(function (item) {
        new Draggable(item, {

          // Set the snap to a grid
          // of 500 pixels
          snap: 500 
        }) });
    }
  </script>
</head>
<body>
    <img id="element" src="gfg.png" />
</body>
</html>
```

**输出:**

![](img/c5e280077afbf060ef85d2176ce0a52a.png)