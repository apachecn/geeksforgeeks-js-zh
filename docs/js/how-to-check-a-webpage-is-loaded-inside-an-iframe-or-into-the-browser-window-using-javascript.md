# 如何使用 JavaScript 检查网页是加载到 iframe 内部还是浏览器窗口中？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 检查网页是否加载到 iframe 或浏览器窗口中/](https://www.geeksforgeeks.org/how-to-check-a-webpage-is-loaded-inside-an-iframe-or-into-the-browser-window-using-javascript/)

一个 **iFrame** 是网页中的一个矩形框或区域，用于加载或显示其中的另一个单独的网页或文档。因此，基本上，iFrame 用于在网页中显示网页。

你可以在这里看到更多关于 **iFrames** 的信息: [HTML iFrames](https://www.geeksforgeeks.org/html-iframes/)

检查网页是否加载到 iFrame 中可能有多种原因，例如，当我们需要动态调整元素的高度或宽度时。

*   **Comparing the object’s location with the window object’s parent location:** Here, we simply compare the object’s location with the window object’s parent location. If the result is *true*, then the webpage is in an iFrame. If it is *false*, then it is not in an iFrame.

    ```
    <script>
    function iniFrame() {
        if ( window.location !== window.parent.location )
        {

            // The page is in an iFrames
            document.write("The page is in an iFrame");
        } 
        else {

            // The page is not in an iFrame
            document.write("The page is not in an iFrame");
        }
    }

    // Calling iniFrame function
    iniFrame();
    </script>
    ```

    **输出:**

    ```
    The page is in an iFrame
    ```

*   **Using *window.top* and *window.self* property:** The *top* and *self* are both window objects, along with *parent*, so check if the current window is the top/main window.

    ```
    <script>

    // Function to check whether webpage is in iFrame
    function iniFrame() {

        if(window.self !== window.top) {

            // !== operator checks whether the operands
            // are of not equal value or not equal type
            document.write("The page is in an iFrame");
        }
        else {
            document.write("The page is in an iFrame");
        }
    }

    // Calling iniFrame function
    iniFrame();
    </script>
    ```

    **输出:**

    ```
    The page is in an iFrame
    ```

*   **Using the *window.frameElement* property:** Note that this only supports webpages belonging to the same origin as the main page in which it is embedded. The function **window.frameElement** returns the element (like iframe and object) in which the webpage is embedded.

    ```
    <script>
    function iniFrame() {

        var gfg = window.frameElement;

        // Checking if webpage is embedded
        if (gfg) {

            // The page is in an iFrame
            document.write("The page is in an iFrame");
        } 
        else {

            // The page is not in an iFrame
            document.write("The page is not in an iFrame");
        }
    }

    // Calling iniFrame function
    iniFrame();
    </script>
    ```

    **输出:**

    ```
    The page is in an iFrame
    ```

    在上面的代码中，将网页嵌入的元素存储到变量 **gfg** 中。如果窗口没有嵌入到另一个文档中，或者如果它嵌入到的文档具有不同的来源(例如来自不同的域)， **gfg** 为空。