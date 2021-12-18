# 如何解析 HTTP Cookie 头并返回一个 JavaScript 中所有 Cookie 名称-值对的对象？

> 原文:[https://www . geesforgeks . org/how-parse-http-cookie-header-and-return-object-of-all-cookie-name-value-pairs-in-JavaScript/](https://www.geeksforgeeks.org/how-to-parse-http-cookie-header-and-return-an-object-of-all-cookie-name-value-pairs-in-javascript/)

[cookie](https://www.geeksforgeeks.org/http-cookies/)只是网络服务器发送给用户浏览器的小文本文件。它们包含以下数据。

1.  具有实际数据的名称-值对。
2.  cookie 失效的到期日期。
3.  它应该发送到的服务器的域和路径。

**方法:**要检索 JavaScript 中存储的所有 cookies，我们可以使用 ***document.cookie** 属性*，但该属性返回一个字符串，其中键值对用“；”分隔。如果我们能够将键值对存储到一个对象中，那就太好了，因为这将使检索过程更加容易。JavaScript 没有为这样的场景提供任何方法。所以让我们来解决这个问题。

我们需要创建一个函数来解析 cookie 字符串，并返回一个包含所有 cookie 的对象。这将是一个具有以下步骤的简单过程。

1.  使用[**string . split(；)从 cookie 字符串中获取每个单独的键值对)** *。*](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)
2.  使用***string . split(“=”***将键与每对中的值分开。
3.  创建一个包含所有键值对的对象，并返回该对象。

**示例:**为了更好的理解，请参考下面代码中的注释。

## java 描述语言

```
<script>
    function cookieParser(cookieString) {

        // Return an empty object if cookieString
        // is empty
        if (cookieString === "")
            return {};

        // Get each individual key-value pairs
        // from the cookie string
        // This returns a new array
        let pairs = cookieString.split(";");

        // Separate keys from values in each pair string
        // Returns a new array which looks like
        // [[key1,value1], [key2,value2], ...]
        let splittedPairs = pairs.map(cookie => cookie.split("="));

        // Create an object with all key-value pairs
        const cookieObj = splittedPairs.reduce(function (obj, cookie) {

            // cookie[0] is the key of cookie
            // cookie[1] is the value of the cookie
            // decodeURIComponent() decodes the cookie
            // string, to handle cookies with special
            // characters, e.g. '{content}apos;.
            // string.trim() trims the blank spaces
            // auround the key and value.
            obj[decodeURIComponent(cookie[0].trim())]
                = decodeURIComponent(cookie[1].trim());

            return obj;
        }, {})

        return cookieObj;
    }

    let dummyCookieString =
        "username=John; gfg=GeeksForGeeks; foo=education";

    // Pass document.cookie to retrieve actual cookies
    let cookieObj = cookieParser(dummyCookieString);

    console.log(`cookie gfg has value ${cookieObj['gfg']}.`);
    console.log(`cookie foo has value ${cookieObj['foo']}.`);
</script>
```

**输出:**

```
cookie gfg has value GeeksForGeeks.
cookie foo has value education.
```