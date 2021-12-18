# 拖动&放下开始效果选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-拖放-starteffect-option/](https://www.geeksforgeeks.org/script-aculo-us-drag-drop-starteffect-option/)

这个脚本用来定义当一个合适的可拖动元素开始被拖动时调用的函数。该函数可用于定义任何效果。

**语法:**

```
{ starteffect: effectFunction }

```

**值:**

*   **效果功能:**该值定义了包含当拖动山墙开始拖动时要显示的效果的功能。

以下示例说明了**拖动&放置开始效果**选项:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="prototype.js">
    </script>

    <script type="text/javascript" 
        src="scriptaculous.js">
    </script>

    <script type="text/javascript">

        window.onload = function () {
            $A($('draggables')
                .getElementsByTagName('img'))
                .each(function (item) {
                    new Draggable(item, {
                        revert: true,

                        // Define the effect to be used
                        // when the dragging starts
                        starteffect: function (element) {
                            new Effect.Opacity(element,
                                {
                                    from: 0,
                                    to: 1.0,
                                    duration: 5
                                })
                        }
                    });
                });
        }
    </script>
</head>

<body style="text-align: center;">
    <div>
        <h1 style="color: green">
            GeeksforGeeks
        </h1>

        <p>A Computer Science Portal
            for Geeks
        </p>
    </div>

    <strong>
        script.aculo.us Drag & Drop
        starteffect Option
    </strong>
    <div id="draggables">
        <img src=
"https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200817185016/gfg_complete_logo_2x-min.png">
    </div>
</body>

</html>
```

**输出:**

![](img/6a4860cfd68bfa7fb1dd2d4fbf53aa65.png)