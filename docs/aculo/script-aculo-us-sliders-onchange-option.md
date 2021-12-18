# 脚本. aculo.us 滑块 onChange 选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-sliders-onchange-option/](https://www.geeksforgeeks.org/script-aculo-us-sliders-onchange-option/)

script.aculo.us 库是一个跨浏览器库，旨在改进网站的用户界面。滑块控件是允许用户输入值的细轨迹。这是通过定义一个值的范围来完成的，用户可以通过将手柄拖动到适当的值来选择该范围。

**onChange** 选项用于指定一个回调函数，每当滑块的值发生变化时，无论是当滑块完成移动时，还是使用 setValue()方法设置新值时，都会调用该回调函数。滑块的当前值将作为参数传递给函数。

**语法:**

```
{ onChange: function }
```

**参数:**该选项具有如上所述的单一值，如下所述:

*   **函数:**这是一个回调函数，每当滑块完成移动或使用 setValue()方法进行更改时，都会调用该函数。

以下示例说明了该选项的使用。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <!-- Include the required scripts -->
  <script type="text/javascript" 
          src="prototype.js">
  </script>
  <script type="text/javascript"
          src="scriptaculous.js?load = slider">
  </script>

  <!-- Style the Sliders so that they
  are properly visible -->
  <style type="text/css">
    .track {
      width: 250px;
      background-color: orange;
      height: 5px;
      position: relative;
    }

    .track .handle {
      width: 20px;
      height: 10px;
      background-color: green;
      cursor: move;
      position: absolute;
      top: -2px;
    }

    .pad {
      padding: 25px 15px;
    }
  </style>
</head>
<body>

<p>
  <h1 style="color: green;">
    GeeksforGeeks
  </h1>
  <h2>Sliders onChange Option</h2>

<p>
    The onChange callback function 
    gets invoked whenever the value
    changes. The value of the slider 
    can be set using the setValue method.
  </p>

  <div class="pad">
    <div id="track-hor" class="track">
      <div id="handle-hor" class="handle">
      </div>
    </div>
  </div>

  <input type="text" id="val">
  <button onclick="setVal()">
    Set Value
  </button>

<p>Current Slider Value: 
    <span id="out">0</span>
  </p>

  <script type="text/javascript">

    // Initialize the slider
    let slider = new Control.Slider('handle-hor',
      'track-hor', {

      // Define the range
      range: $R(1, 100),

      onChange: function (currValue) {
        document.querySelector("#out")
                  .textContent = currValue;
      }
    });

    function setVal() {

      // Get the value form the input box
      let val =
          document.querySelector("#val")
                    .value;

      // Set the value of the slider
      // to the given value
      slider.setValue(val);
    }
  </script>
</body>
</html>
```

**输出:**

![](img/22e404be4c273978ab2d4e8bc1406e71.png)