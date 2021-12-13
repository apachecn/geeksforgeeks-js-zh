# 如何使用 JavaScript 创建一个到任何网站的常见问题部分？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 创建任何网站的常见问题部分/](https://www.geeksforgeeks.org/how-to-create-an-faq-section-to-any-website-using-javascript/)

在本文中，我们使用 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 创建了一个常见问题(FAQ)手风琴。手风琴用于以列表格式显示内容。它可以*展开*或*折叠*来显示它包含的内容。

**方法:**

*   Create a nested HTML [div](https://www.geeksforgeeks.org/div-tag-html/) tag with the class name containing the question and answer.
*   For styles, add some [CSS](https://www.geeksforgeeks.org/css-tutorials/) attributes, such as alignment, font size, padding, margins, etc.
*   Use JavaScript to realize the function of displaying answers or folding items when clicking questions.

**HTML 代码:**我们已经使用类进行问答。这些类用于样式目的。

## 【index.html】

```html
<!DOCTYPE html>
<html>

<head>
  <link rel="stylesheet" href="styles.css">
  <script src="main.js"></script>
</head>

<body>
  <h2 style="color:green; text-align:center">
    GeeksforGeeks
  </h2>
  <div class="layout">
    <div class="accordion">
      <div class="accordion__question">
        <p>Where is Taj Mahal located?</p>

      </div>
      <div class="accordion__answer">
        <p>Taj Mahal is located in Agra, Uttar Pradesh.</p>
      </div>
    </div>

    <div class="accordion">
      <div class="accordion__question">
        <p>How many planets are there in solar system?</p>
      </div>

      <div class="accordion__answer">
        <p>
          There are eight planets in solar system.
          Mercury, Venus, Earth, Mars, Jupiter, Saturn,
          Uranus, and Neptune.
        </p>
      </div>
    </div>
  </div>
</body>

</html>
```