# 如何在 JavaScript 中创建查询参数？

> 原文:[https://www . geesforgeks . org/如何创建查询参数 in-javascript/](https://www.geeksforgeeks.org/how-to-create-query-parameters-in-javascript/)

任务是使用 javaScript 为给定的 JSON 对象创建 **GET** 请求的查询网址。获取一个网址中的查询参数只是一串与符号&相连的键值对。要将 JSON 对象转换为 GET 查询参数，我们可以使用以下方法。

*   进行变量查询。
*   循环遍历 json 的所有键和值，并用' & '符号将它们连接在一起。

**示例:**

```
Input: {'website':'geeks', 'location':'india'}
Output: website=geeks&location=india
```

**语法:**

```
function encodeQuery(data){
    let query = ""
    for (let d in data)
         query += encodeURIComponent(d) + '=' + 
            encodeURIComponent(data[d]) + '&'
    return query.slice(0, -1)
}
```

以下示例实现了上述方法:

**例 1:**

```
<script>
function encodeQuery(data){
    let query = ""
    for (let d in data)
         query += encodeURIComponent(d) + '=' 
                  + encodeURIComponent(data[d]) + '&'
    return query.slice(0, -1)
}

// Json object that should be
// converted to query parameter
data = { 
    'website':'geeks',
    'location':'india'
}
queryParam = encodeQuery(data)
console.log(queryParam)
</script>
```

**输出:**

```
website=geeks&location=india
```

**示例 2:** 在本例中，我们将根据给定的 JSON 数据创建一个完整的 URL。

```
<script>
function encodeQuery(data){
    let query = data.url
    for (let d in data.params)
         query += encodeURIComponent(d) + '='
              + encodeURIComponent(data.params[d]) + '&';
    return query.slice(0, -1)
}

// Json object that should be
// converted to query parameter
data = { 
    url : 'www.geeksforgeeks.com/',
    params : {
        'website':'geeks',
        'location':'india'
    }
}
queryParam = encodeQuery(data)
console.log(queryParam)
</script>
```

**输出:**

```
www.geeksforgeeks.com/website=geeks&location=india
```