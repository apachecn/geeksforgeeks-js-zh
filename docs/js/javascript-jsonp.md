# JavaScript | JSONP

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-jsonp/

**什么是 JSONP？**
XMLHttpRequest(XHR)可以用来从服务器获取数据。一旦在浏览器中接收到数据，它就可以使用 JSON.parse()方法将接收到的 JSON 字符串转换成 JavaScript 对象。但是，XHR 也有同样的安全问题。这意味着，从某个域请求一个页面，比如说 ADomain.com，然后这个页面发出一个 XMLHttpRequest，从 BDomain.com 获取一些数据，浏览器拒绝了这个请求。这是因为该请求是向不同于提供页面的域发出的。只有当 XMLHttpRequest 向 ADomain.com 发出时，它才会接收回数据，因为 XHR 只有在向同一个域发出请求时才能工作。

**JSONP(带填充的 JSON):**通过避免跨域问题来检索数据的一种方式。*脚本*标签就是用来这样做的。

【JSON 和 JSONP 的区别:

*   **JSON:** JavaScript 使用 JSON (JavaScript 对象符号)在网络上交换数据。它仔细观察一个 JSON 数据，它只是一个字符串格式的 JavaScript 对象。
    T3】例:

```
{"name":"GFG", "id":1, "articlesWritten":5}
```

*   **JSONP:** JSONP is JSON with Padding. Here, padding means wrapping a function around the JSON before it comes back in the request.
    **Example:**

    ```
    GeeksFunction({"name":"GFG", "id":1, "articlesWritten":5});
    ```

    **使用 JSONP 的方法:**

    *   在 HTML 代码中，包含脚本标签。该脚本标记的来源将是从中检索数据的 URL。web 服务允许指定回调函数。在网址的最后包含回调参数。
    *   当浏览器遇到脚本元素时，它会向源 URL 发送 HTTP 请求。
    *   服务器用包装在函数调用中的 JSON 发回响应。
    *   浏览器解析字符串形式的 JSON 响应，并将其转换为 JavaScript 对象。回调函数被调用，生成的对象被传递给它。

    **例 1:**

    ```
    <!DOCTYPE html>
    <html>
    <body>
        <p id="paragraphElement"></p>

        <!-- The server returns a call to the callback function
        (processData) that will handle the JSON data -->
        <script>
            function processData(myObj) {
            console.log(myObj);
            var para= document.getElementById("paragraphElement");
            for(var i=0; i<myObj.resultCount; i++){
                para.innerHTML= para.innerHTML + myObj.results[i].trackName
                                + "<br>" ; 
                } 
            }
        </script>

    <!-- Calling the iTunes API to search for Jack Johnson's songs and return 
            the first five items -->
        <script src="https://itunes.apple.com/search?term=jack+johnson&limit=5
        &callback=processData"></script>
    </body>
    </html>                    
    ```

    **输出:**

    ```
    Better Together
    Banana Pancakes
    Sitting, Waiting, Wishing
    Upside Down
    Good People
    ```

    **示例 2:** 使用 JavaScript 动态添加脚本元素

    ```
    <!DOCTYPE html>
    <html>
    <body>
        <p id="paragraphElement"></p>

        <script>
        window.onload = createScriptDynamically();
        function createScriptDynamically() {

            // Set the url to the web service API from where 
            // the data to be retrieve
            var url = 
            "https://itunes.apple.com/search?term=taylor+swift&limit=5&callback=processData";

            // Create the script element dynamically through JavaScript 
            var scriptElement = document.createElement("script");

            // Set the src and id attributes of the script element
            scriptElement.setAttribute("src", url);
            scriptElement.setAttribute("id", "jsonp");
            var oldScriptElement= document.getElementById("jsonp");

            // Get the head element
            var head = document.getElementsByTagName("head")[0];
            if(oldScriptElement == null) {         

                /* If there is no script element then append
                a new element to the head. */
                head.appendChild(scriptElement);
            }
            else {

                /* If there is already a element in the head, 
                then replace it with the new script element. */
                head.replaceChild(scriptElement, oldScriptElement); 
            } 
        }

        function processData(myObj) {
            console.log(myObj);

            /* Function to display the track name and the
            genre name from the received data. */
            var para = document.getElementById("paragraphElement");

            for(var i = 0; i < myObj.resultCount; i++){
                para.innerHTML = para.innerHTML + myObj.results[i].trackName 
                   + "[" + myObj.results[i].primaryGenreName + "]" + "<br>" ; 
            } 
        }
    </script>
    </body>
    </html>                    
    ```

    **输出:**

    ```
    Delicate [Pop]
    Look What You Made Me Do [Pop]
    Shake It Off [Pop]
    You Belong With Me [Country]
    Blank Space [Pop]
    ```