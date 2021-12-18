# JSON 中如何处理换行符？

> 原文:[https://www . geesforgeks . org/how-handle-new lines-in-JSON/](https://www.geeksforgeeks.org/how-to-handle-newlines-in-json/)

JSON 是一种独立于语言的数据格式。这是一个 JavaScript 对象符号。基本上，它是一种基于文本的格式，用于表示结构化数据。数据以这种格式从服务器发送到客户端。

在本文中，我们将看到如何在 JSON 中处理换行符。

**语法:**

```
'\\n'
```

**关于“\ \ n”:**每当我们想要以 JSON 格式多行发送数据时，都会用到上面的语法。一般来说，很难用新的线路从服务器向网络发送数据。但是通过使用它，我们可以达到以下要求。

**进场:**

*   首先，我们需要将一个变量声明为“json1”，然后我们需要将 json 分配给它。
*   在 JSON 对象中，确保您有一个句子需要用不同的行打印。
*   现在为了打印不同行的语句，我们需要使用“\\n”(反斜杠)。
*   正如我们现在知道的用换行符打印的技术，现在只要在任何你想要的地方加上“\\n”就可以了。
*   现在，由于它是一个 JSON，我们需要解析它来打印它。所以使用 JSON.parse()方法，解析 JSON。
*   完成上述步骤后，编写 console.log()语句来打印输出。
*   完成后，执行文件以获得输出。

**代码实现:**

**例 1:**

## java 描述语言

```
var json = '{
    "companyInfo" : 
    "GeeksForGeeks\\n\\nOne stop solution for CS subjects"
}';            

let finalJson=JSON.parse(json);

console.log(finalJson.companyInfo)
```

**输出:**

```
GeeksForGeeks

One stop solution for CS subjects
```

**例 2:**

## java 描述语言

```
var student = '{
    "details" : 
    "P.V.Ramesh\\nC.S.E.\\nI.I.T. Hyderabad"
}';

let finalJson = JSON.parse(student);

console.log(finalJson.details)
```

**输出:**

```
P.V.Ramesh
C.S.E.
I.I.T. Hyderabad
```