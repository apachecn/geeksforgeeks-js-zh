# JavaScript 自定义事件

> 原文:[https://www.geeksforgeeks.org/javascript-custom-events/](https://www.geeksforgeeks.org/javascript-custom-events/)

几乎每个 web 应用程序都使用事件，例如 **onclick 事件**用于在用户点击某个东西时执行一些代码。已经有许多内置事件可供使用，但是如果我们想要自己的自定义事件呢？让我们假设我们正在创建一个聊天应用程序，我们希望在终端用户发送消息时执行一些代码。没有内置事件来检测这一点。这里我们需要一个可以处理这种自定义场景的自定义事件。

**创建自定义事件:**要创建自定义事件，我们使用**事件**构造函数或**自定义事件**界面。事件构造函数创建一个事件，客户事件创建一个具有更多功能的事件。

遵循以下步骤，使用新的**事件**创建一个。

*   我们使用事件构造函数创建一个事件。
*   我们使用 **addEventListener()** 方法来监听这个事件。
*   我们使用**元素触发或调度事件。**
*   名为**开始**的自定义事件现已创建。

**语法:**

```
// To assign event
const startEvent = new Event("start");

// To trigger the event Listener
document.addEventListener("start", () => {
    console.log("The start event was triggered")
});

// To trigger the Event
document.dispatchEvent(startEvent);
```

**示例:**在本例中，我们正在创建一个当 **x** 的值为 5 时触发的事件。

## 超文本标记语言

```
<html>
<body>
  <script>
    let x = 5;
    const event = new Event("start");

    document.addEventListener('start', ()=>{
      console.log("Start event triggered")
    });

    if(x == 5){
      document.dispatchEvent(event);
    }
  </script>
</body>
</html>
```

**输出:**

```
"Start event triggered"
```

**使用 custom event 创建自定义事件:**使用 CustomEvent 接口创建自定义事件具有优势，因为它可以发送自定义数据。按照以下步骤创建新的客户事件。

*   我们使用 custom event 构造函数创建一个自定义事件。
*   这需要两个参数，第一个是事件的名称，第二个是包含数据的对象。对象名里面的属性名要命名为**明细**否则不起作用。
*   我们为此事件创建一个侦听器。
*   我们触发或发送事件。
*   已创建包含数据的自定义事件。

**语法:**

```
// To assign event
const event = new CustomEvent("start", {
      detail: {
        platform : "GeeksforGeeks"
      }
});

// To trigger the event Listener
document.addEventListener('start', (e)=>{
      console.log(
        `start event triggered on platform :
        ${e.detail.platform}`
        );
});

// To trigger the Event
document.dispatchEvent(event);
```

**示例 2:** 在本例中，我们创建了一个自定义事件，当 **x** 的值为 5 时触发。

## 超文本标记语言

```
<html> 
<body>
  <script>
    let x = 5;
     const event = new CustomEvent("start", {
      detail: {
        platform : "GeeksforGeeks"
      }
    });

    document.addEventListener('start', (e) => {
      console.log(
        `Start event triggered on platform
        ${e.detail.platform}`
      );
    })

    if (x == 5) {
      document.dispatchEvent(event);
    }
  </script>
</body>
</html>
```

**输出:**

```
Start event triggered on platform GeeksforGeeks
```

**注意:**我们使用**document . dispatchevent(' start ')**、直接从文档中调度事件，但是可以从任何需要的元素中调度事件，如**mybtn . dispatchevent(' start ')**。