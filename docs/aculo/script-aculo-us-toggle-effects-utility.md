# 脚本 aculo.us 切换效果实用程序

> 原文:[https://www . geesforgeks . org/script-aculo-us-toggle-effects-utility/](https://www.geeksforgeeks.org/script-aculo-us-toggle-effects-utility/)

切换效果实用程序用于切换带有附加动画的元素。支持三个动画道具*出现*、*失明*和*滑动*。

*   **出现:**模拟*出现效果*模块隐藏和显示元素
*   **滑动:**模拟*向上滑动*、*向下滑动*效果模块进行隐藏和
    展示元素。
*   **Blind:** 模拟 *BlindUp* 和 *BlindDown* 效果模块进行隐藏和
    元素展示。

**语法:**

```
Effect.toggle(element_id, Animation Prop, {options} );
```

**示例:**

```
<!DOCTYPE html>
<html>

<head>
    <script type="text/javascript" 
        src="./javascript/prototype.js">
    </script>

    <script type="text/javascript" 
src="./javascript/scriptaculous.js?load = effects">
    </script>

    <script>
        function AppearEffect(element) {
            new Effect.toggle(element, 'Appear', {
                duration: 3
            });
        }

        function BlindEffect(element) {
            new Effect.toggle(element, 'Blind', {
                duration: 3
            });
        }

        function SlideEffect(element) {
            new Effect.toggle(element, 'Slide', {
                duration: 3
            });
        }
    </script>
</head>

<body>
    <div>
        <Button onclick="AppearEffect('element')"> 
                 Appear Effect</Button>
        <Button onclick="SlideEffect('element')"> 
                 SlideEffect</Button>
        <Button onclick="BlindEffect('element')"> 
                 BlindEffect</Button>
    </div>

    <div id='element'>
        <img src="gfg.png" />
    </div>
</body>

</html>
```

**输出:**
![](img/2548157b8ff5b543ad13551f988f283c.png)