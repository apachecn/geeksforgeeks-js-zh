# 读取 XML 文件，使用 JavaScript 将详细信息打印为表格数据

> 原文:[https://www . geesforgeks . org/read-XML-file-and-print-details-as-table-data-by-use-JavaScript/](https://www.geeksforgeeks.org/read-xml-file-and-print-the-details-as-tabular-data-by-using-javascript/)

**简介:**使用 javaScript 读取 XML 文件，以表格形式打印 XML 文件的详细信息。我们需要创建一个想要打印哪些数据的 XML 文件。XML 代表可扩展标记语言。它是一种与 HTML 非常相似的标记语言。XML 文件的主要用途是用来存储和传输数据。创建一个 XML 文件非常简单，因为它使用自定义标签。

**先决条件:**

*   [基础知识](https://www.geeksforgeeks.org/html-tutorials/) [HTML](https://www.geeksforgeeks.org/html-tutorials/)
*   [基础知识](https://www.geeksforgeeks.org/css-tutorials/) [CSS](https://www.geeksforgeeks.org/css-tutorials/)
*   [基础知识](https://www.geeksforgeeks.org/javascript-tutorial/) [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/)
*   [知识](https://www.geeksforgeeks.org/xml-basics/)T2【XML

**方法:**创建 XML 文件后，我们将编写 JavaScript 以表格形式从文件中读取和提取数据。因此，我们将把 XMLHttpRequest 发送到服务器，并使用 JavaScript 从 XML 文件中获取详细信息。如果请求完成了，那么响应就准备好了，并且状态是“好的”，所以我们通过使用标记名来获取 XML 数据。

现在我们将创建两个文件:

**1.employee.xml:** 存储员工详细信息的 xml 文件。为了创建一个 xml 文件，我们使用自定义标签，这里我们使用不同的自定义标签，如名字、姓氏、头衔、部门等。它根据标签名存储每个员工的详细信息。

## employee.xml

```html
<?xml version="1.0" encoding="utf-8"?>
<employees>
    <employee id="be129">
        <firstname>Jitendra</firstname>
        <lastname>Kumar</lastname>
        <title>Engineer</title>
        <division>Materials</division>
        <building>327</building>
        <room>19</room>
    </employee>
    <employee id="be130">
        <firstname>Amit</firstname>
        <lastname>Kumar</lastname>
        <title>Accountant</title>
        <division>Accts Payable</division>
        <building>326</building>
        <room>14</room>
    </employee>
    <employee id="be131">
        <firstname>Akash</firstname>
        <lastname>Kumar</lastname>
        <title>Engineering Manager</title>
        <division>Materials</division>
        <building>327</building>
        <room>21</room>
    </employee>
    <employee id="be132">
        <firstname>Aishwarya</firstname>
        <lastname>Kulshrestha</lastname>
        <title>Engineer</title>
        <division>Materials</division>
        <building>327</building>
        <room>22</room>
    </employee>
    <employee id="be133">
        <firstname>Sachin</firstname>
        <lastname>Kumar</lastname>
        <title>Engineer</title>
        <division>Materials</division>
        <building>327</building>
        <room>24</room>
    </employee>
    <employee id="be135">
        <firstname>Vikash</firstname>
        <lastname>kumar</lastname>
        <title>COO</title>
        <division>Management</division>
        <building>216</building>
        <room>26</room>
    </employee>
    <employee id="be136">
        <firstname>Suvam</firstname>
        <lastname>Basak</lastname>
        <title>Accountant</title>
        <division>Accts Payable</division>
        <building>326</building>
        <room>30</room>
    </employee>
    <employee id="be135">
        <firstname>Abhinav</firstname>
        <lastname>kumar</lastname>
        <title>COO</title>
        <division>Management</division>
        <building>216</building>
        <room>32</room>
    </employee>
     <employee id="be131">
        <firstname>DhanPal</firstname>
        <lastname>Singh</lastname>
        <title>Engineering Manager</title>
        <division>Materials</division>
        <building>327</building>
        <room>21</room>
    </employee>

</employees>
```

**2.index.html:** 这个文件包含了 html、CSS 和 JavaScript 代码。我们在 CSS 部分使用样式标签，在 CSS 部分，我们设置表格属性和按钮的样式，然后我们使用脚本标签，在脚本标签中我们编写 JavaScript 代码并插入 employee.xml 文件。在 loadXMLDoc()函数中，我们向服务器发送 HTTP 请求，当请求完成时，我们从服务器获得响应，并从 XML 文件中访问数据。在 empDetails()函数中，如果我们从服务器获得响应，那么我们通过使用自定义标记名逐个获取 XML 文件数据。要显示这个 xml 文件的数据，我们只需单击“获取员工详细信息”按钮，xml 文件数据就会以表格形式显示在您的屏幕上。

## index.html

```html
<!DOCTYPE html>

<head>
    <title>Reads the XML data using JavaScript</title>

    <!-- CSS -->
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
        }

        th,
        td {
            text-align: left;
            padding: 8px;
        }

        tr:nth-child(even) {
            background-color: #7ce2af
        }

        th {
            background-color: #7c0f65;
            color: white;
        }

        .button {
            position: relative;
            text-align: center;
            padding: 20px;
            border: 4px solid rgb(55, 12, 211);
            background: rgba(20, 192, 4, 0.5);
            color: rgb(230, 36, 78);
            outline: none;
            border-radius: 30px;
            font-size: 30px;
            width: 500px;

        }

        .button:hover {
            color: black;
            background: white;
        }
    </style>

    <!--JavaScript-->
    <script>
        function loadXMLDoc() {
            var xmlhttp = new XMLHttpRequest();
            xmlhttp.onreadystatechange = function () {

                // Request finished and response 
                // is ready and Status is "OK"
                if (this.readyState == 4 && this.status == 200) {
                    empDetails(this);
                }
            };

            // employee.xml is the external xml file
            xmlhttp.open("GET", "employee.xml", true);
            xmlhttp.send();
        }

        function empDetails(xml) {
            var i;
            var xmlDoc = xml.responseXML;
            var table =
                `<tr><th>Firstname</th><th>Lastname</th>
                    <th>Title</th><th>Division</th>
                    <th>Building</th><th>Room</th>
                </tr>`;
            var x = xmlDoc.getElementsByTagName("employee");

            // Start to fetch the data by using TagName 
            for (i = 0; i < x.length; i++) {
                table += "<tr><td>" +
                    x[i].getElementsByTagName("firstname")[0]
                    .childNodes[0].nodeValue + "</td><td>" +
                    x[i].getElementsByTagName("lastname")[0]
                    .childNodes[0].nodeValue + "</td><td>" +
                    x[i].getElementsByTagName("title")[0]
                    .childNodes[0].nodeValue + "</td><td>" +
                    x[i].getElementsByTagName("division")[0]
                    .childNodes[0].nodeValue + "</td><td>" +
                    x[i].getElementsByTagName("building")[0]
                    .childNodes[0].nodeValue + "</td><td>" +
                    x[i].getElementsByTagName("room")[0]
                    .childNodes[0].nodeValue + "</td></tr>";
            }

            // Print the xml data in table form
            document.getElementById("id").innerHTML = table;
        }
    </script>
</head>

<body>
    <center>
        <button type="button" class="button" 
            onclick="loadXMLDoc()">
            Get Employees Details
        </button>
    </center>

    <br><br>
    <table id="id"></table>
</body>

</html>
```

**运行应用程序的步骤:**要读取 XML 数据，我们需要在本地服务器上运行这段代码因此，首先我们启动本地服务器，在它打开 chrome 浏览器后，启动本地主机并查看结果。点击获取员工详细信息按钮后，我们会以表格形式获取员工详细信息。

**输出:**

![](img/8b921a5b5188333a92409dcec6626778.png)