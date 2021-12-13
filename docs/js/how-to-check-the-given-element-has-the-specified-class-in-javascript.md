# 如何在 JavaScript 中检查给定的元素是否有指定的类？

> 原文:[https://www . geesforgeks . org/如何检查给定元素是否有指定的 javascript 类/](https://www.geeksforgeeks.org/how-to-check-the-given-element-has-the-specified-class-in-javascript/)

有时我们需要检查元素是否有类名' **X'** (任意具体名称)。要检查元素是否包含特定的类名，我们可以使用 **classList** 对象的 **contains** 方法。

#### 语法:

```html
element.classList.contains("class-name")
```

它返回一个**布尔**值。如果元素包含类名，则返回 **true** 否则返回 **false。**

**实现:**现在我们来实现给定的方法。在这里，我们将创建一个简单的 HTML 页面，并添加一个 h1 元素，其类名为 **main** ，id 名为 **main。**我们的任务是找到 h1 包含的类名 main。

## HTML

```html
<!DOCTYPE html>
<html>

<body>
    <h1 id="main" class="main">Welcome To GFG</h1>
</body>

</html>
```