# 拖动&放下悬停类选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-拖放-悬停类-option/](https://www.geeksforgeeks.org/script-aculo-us-drag-drop-hoverclass-option/)

这个 script.aculo.us 拖放悬停类选项用于创建一个活动的悬停类，您可以在其中将一个可拖动的元素拖动到拖放区域。在拖放区，将放置元素。这是一个 CSS 类的名称，当可删除选项处于活动状态时，它将被添加到元素中。

**语法:**

```
Droppables.add('element', {hoverclass: 'cssClass'});
```

**示例:**下面的示例说明了拖放悬停类选项。

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="scriptaculous-js-1.9.0/lib/prototype.js">
    </script>

    <script type="text/javascript" 
        src="scriptaculous-js-1.9.0/src/scriptaculous.js">
    </script>

    <script type="text/javascript">
        window.onload = function () {
            $A($("draggables").getElementsByTagName(
                "img")).each(function (item) {
                    new Draggable(
                        item, { revert: true, ghosting: true });
                });

            Droppables.add(
                "droparea", {
                    hoverclass: "hoverActive",
                onDrop: moveItem
            });

            // Set drop area default non cleared.
            $("droparea").cleared = false;
        };

        function moveItem(draggable, droparea) {
            if (!droparea.cleared) {
                droparea.innerHTML = "";
                droparea.cleared = true;
            }

            draggable.parentNode.removeChild(draggable);
            droparea.appendChild(draggable);
        }
    </script>

    <style type="text/css">
        #draggables {
            width: 550px;
            height: 73px;
        }

        #droparea {
            float: left;
            width: 550px;
            height: 73px;
            border: 2px solid gray;
            text-align: center;
            font-size: 16px;
            padding: 12px;
        }
    </style>
</head>

<body>
    <div>
        <h1 style="color: green;">GeeksforGeeks</h1>

        <p>A Computer Science Portal for Geeks</p>

    </div>
    <strong>
        script.aculo.us Drag & Drop hoverclass Option
    </strong>
    <div id="draggables">
        <img src="gfg.png" />
    </div>
    <div id="droparea">
        Drag the Image and Drop Your Image in this area
    </div>
</body>

</html>
```