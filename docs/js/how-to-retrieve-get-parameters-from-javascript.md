# 如何从 JavaScript 中检索 GET 参数？

> 原文:[https://www . geesforgeks . org/如何从 javascript 中检索获取参数/](https://www.geeksforgeeks.org/how-to-retrieve-get-parameters-from-javascript/)

为了知道参数，那些都是通过**【GET】**方法传递的，就像有时候我们传递 Email-id、Password 等细节一样。为此，我们使用以下代码片段。

当你访问任何网站时，有没有想过问号是什么？正在地址栏里做什么。让我们看看这个问号有什么用？。

**什么是“？”:**T3】

问号就像一个分隔符，后面是一个键值对形式的查询字符串。多个键值对由“&”符号分隔。

**示例:**

```
geeksforgeeks.org/web-development?page=2&name=gfg
```

上图为地址。后跟“？”的内容是具有两个键值对的查询字符串，如下所示:

*   第一对:第二页
*   第二对:名称= gfg

我们的任务是从每对中获取各自的值，这些值也被称为 get 参数。

**方法 1:** **使用地址中指定的键:**类 URLSearchParams 接受网站的地址，并搜索与提供的键相关联的值。

以下是上述方法的代码:

## java 描述语言

```
// Arrow function to get the parameter
// of the specified key
getParameter = (key) => {

    // Address of the current window
    address = window.location.search

    // Returns a URLSearchParams object instance
    parameterList = new URLSearchParams(address)

    // Returning the respected value associated
    // with the provided key
    return parameterList.get(key)
}

// Gets the value associated with the key "ie"
console.log(getParameter("ie"))
```

**输出:**

```
2
```

**方法 2:** 使用 URLSearchParams 类的 forEach 属性检索所有 GET 参数。

## java 描述语言

```
// Arrow function to get all the GET parameters
getParameters = () => {

    // Address of the current window
    address = window.location.search

    // Returns a URLSearchParams object instance
    parameterList = new URLSearchParams(address)

    // Created a map which holds key value pairs
    let map = new Map()

    // Storing every key value pair in the map
    parameterList.forEach((value, key) => {
        map.set(key, value)
    })

    // Returning the map of GET parameters
    return map
}

// Gets all the getParameters
console.log(getParameters())
```

**输出:**

```
{"page" => "2", "name" => "gfg"}
```