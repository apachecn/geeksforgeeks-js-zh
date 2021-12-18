# 使用 JavaScript 中的 Fetch GET 请求(Fetch API)从 JSON 数据创建图表

> 原文:[https://www . geesforgeks . org/create-a-chart-from-JSON-data-use-fetch-get-request-fetch-API-in-JavaScript/](https://www.geeksforgeeks.org/create-a-chart-from-json-data-using-fetch-get-request-fetch-api-in-javascript/)

在本文中，我们将通过使用 Fetch API 的 [Fetch()方法](https://www.geeksforgeeks.org/javascript-fetch-method/)获取 JSON 数据来创建一个简单的图表。提取应用编程接口允许我们以更简单的方式处理 HTTP 请求。

**fetch()方法:**fetch 方法获取一个资源，从而返回一个承诺，一旦响应可用，该承诺就会实现。

**语法:**

```
const response = fetch(resource [, init])
```

**参数:**

*   **资源:**资源的路径(也可以是本地文件)
*   **init:** 您想要添加的任何其他选项，如标题、正文、方法等。

**方法:**步骤可描述如下:

**步骤 1:** 第一步是通过指定资源的路径来调用 fetch 函数。在本例中，我们将使用网址中的免费资源，如下所示:

> "https://datausa.io/api/data？明细=国家和计量=人口

它包含了美国不同年份的人口。响应对象如下所示:

> 回应{
> 类型:“cors”，
> URL:"https://datausa.io/api/data？明细=国家&措施=人口】，
> 重定向:假，
> 状态:200，
> 正常:真，
> 状态文本:“正常”，
> 标头:标头，
> 正文:ReadableStream，
> 正文:true
> }
> 正文:ReadableStream {锁定:true }
> 正文:true
> 标头:{标头}
> 正常:true
> 重定向:假
> 状态:220 明细=国家&度量=人口"
> <原型>:响应协议类型{克隆:克隆()、数组缓冲区:数组缓冲区()、blob: blob()、… }

**步骤 2:** 然后我们将在数据流中得到一个结果。然后，我们查看我们的 JSON 数据，如下所示:

> 对象{数据:(7)[……]，来源:(1)[……]}
> 数据:数组(7)[{……}，{……}，{……}，……]
> 0:对象{
> 【ID 国】:【01000US】，
> 国:【美国】，
> 【ID 年】:2019，……
> }
> 【ID 国】:【01000 us】
> 【ID 年】:2019
> 国:】
> 【身份证年份】:2018、…
> }
> 2:对象{
> 【身份证民族】:01000US、
> 民族:【美国】、
> 【身份证年份】:2017、…
> }
> 3:对象{
> 【身份证民族】:01000US、
> 民族:【美国】、
> 【身份证年份】:2016、…【身份证 …
> }
> 6:对象{
> 【ID 国】:【01000US】、
> 国:【美国】、
> 【ID 年】:2013、…
> }
> 长度:7
> <原型>:数组[]
> 来源:数组{…}
> <原型>:对象{…}

如你所见，我们有一个长度为 7 的数组。每个对象都有几个属性。在这些属性中，我们只是使用 for 循环将两个属性(即年份和人口)存储到两个不同的数组中。

**第 3 步:**最后一步是我们根据收到的数据创建图表。为此，我们使用了 chart.js，这是一种在我们的网站上包含图表的简单方法。在你的头像标签中添加 CDN 链接