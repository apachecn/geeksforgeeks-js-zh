# 如何在 JavaScript 中将 CSV 转换为 JSON 文件，反之亦然？

> 原文:[https://www . geesforgeks . org/how-convert-CSV-to-JSON-file-反之亦然-in-javascript/](https://www.geeksforgeeks.org/how-to-convert-csv-to-json-file-and-vice-versa-in-javascript/)

CSV 文件是一种常见的文件格式，用于以类似表格的方式存储数据。当用户打算下载结构化信息时，它们可能特别有用，因为用户可以在本地机器上轻松打开和阅读结构化信息。CSV 文件非常适合这种情况，因为它们具有可移植性和通用性。

在本文中，我们将解释如何将 JavaScript 对象 JSON 转换为 CSV 文件格式，反之亦然。这段代码不使用任何外部库，因此它可以在浏览器和 Node.js 上工作

#### 从 JSON 转换为 CSV

要从 JSON 转换为 CSV，我们首先需要识别 CSV 文件的头。为此，让我们获取一个已经传入的每个 JavaScript 对象中存在的键的列表。要获取这个键列表，请使用“Object.keys()”方法。

## Javascript

```
<script>
    const JSONToCSV = (objArray, keys) => {
        let csv = keys.join(',');
        objArray.forEach((row) => {
            let values = [];
            keys.forEach((key) => {
                values.push(row[key] || '');
            });
            csv += '\n' + values.join(',');
        });
        return csv;
    };

    const exampleJSON = [
        { 
            "date": 20210307, 
            "positives": 28756184, 
            "fatalities": 515148 
        },
        { 
            "date": 20210306, 
            "positives": 28714654, 
            "fatalities": 514309 
        },
        { 
            "date": 20210305, 
            "positives": 28654639, 
            "fatalities": 512629 
        },
        { 
            "date": 20210304, 
            "positives": 28585852, 
            "fatalities": 510408 
        },
        { 
            "date": 20210303, 
            "positives": 28520365, 
            "fatalities": 508665 
        },
        { 
            "date": 20210302, 
            "positives": 28453529, 
            "fatalities": 506216 
        },
        { 
            "date": 20210301, 
            "positives": 28399281, 
            "fatalities": 504488 
        }
    ];
    console.log(JSONToCSV(exampleJSON, 
        ['date', 'positives', 'fatalities']));
</script>
```