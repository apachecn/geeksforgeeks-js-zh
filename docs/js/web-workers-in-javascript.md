# Javascript 中的网络工作者

> 原文:[https://www.geeksforgeeks.org/web-workers-in-javascript/](https://www.geeksforgeeks.org/web-workers-in-javascript/)

网络工作者给了我们编写多线程 Javascript 的可能性，它不会阻塞 DOM。甚至异步操作也在某种程度上阻塞了 DOM。另一方面，网络工作者帮助我们解决了这个问题，摆脱了单线程环境，达到了更高的网页性能。

**使用顺序:**

*   网络工作者生活在他们自己的文件中*(不与用户界面交互)**   功能是*通过复制**   No global variables are allowed

    **实现网络工作者**

    ```
    /* -----------------------------Index.JS--------------------------*/

      // Check if web worker functionality is available for the browser
            if(window.Worker){

                // Creating new web worker using constructor
                var worker = new Worker('worker.js');

                var message = 'Hello';

                // Sending the message using postMessage
                worker.postMessage(message);

                // On response
                worker.onmessage = function(e) {
                    console.log(e.data);
                };

            }

    /* -----------------------------Worker.JS--------------------------*/

    // Waits for any activity from the page
    self.onmessage = function(e) {
        if(e.data !== undefined) {
            // Do work 
            var total = e.data + ' World';
            // Posting back to the page
            self.postMessage(total)
        }
    }
    // Terminate with: worker.terminate()
    ```

    在上面的示例中，工作人员正在将接收到的字符串与定义的字符串连接起来，并将其发送回 main.js 文件，而不会中断页面。

    ```
    Output :'Hello World'

    ```

    **网络工作者无权访问:**

    *   父对象*   窗口对象*   文档对象*   The DOM

    **但是，可以访问:**

    *   位置对象*   导航器对象*   XMLHttpRequest*   应用程序缓存*   产生其他网络工作者*(与父页面存储在同一原点)**   Importing external script using importScripts()

    **常用用例:**

    *   当需要复杂的计算时*   在 HTML5 游戏中*(更高的帧率)**   At any websites containing JavaScript for performance improvement

    **真实世界示例**

    编写以下程序的原因是为了显示我们的页面在有和没有 worker 时的行为有什么不同。

    ```
    /* -----------------------------Index.JS--------------------------*/
    const delay = 5000;

    // Get element of without worker button
    const noWorkerBtn = document.getElementById('worker--without');
    // Add event listener to the button itself
    noWorkerBtn.addEventListener('click', () => {
        // Define the starting time
        const start = performance.now();
        // Do complex calculations
        while (performance.now() - start < delay);
        // Get the ending time
        const end = performance.now();
        // Calculate the difference in time
        const resWithoutWorker = end - start;
        // Log the result
        console.log('No worker:', resWithoutWorker);

    });

    // Define a worker
    const worker = new Worker('./worker.js');

    // Get element of with worker button
    const workerBtn = document.getElementById('worker--with');

    // Add event listener to the button
    workerBtn.addEventListener('click', () => {
        // Send delay number
        worker.postMessage(delay);

    });
    // On message from worker
    worker.onmessage = e => {
        // Log the result
        console.log("With worker: ", e.data);
    };

    /* -----------------------------Worker.JS--------------------------*/

    // On message received
    this.onmessage = e => {
        // Delay equals to data received
        const delay = e.data;
        // Define starting time
        const start = performance.now();
        // Do the complex calculation
        while (performance.now() - start < delay);
        // Get ending time
        const end = performance.now();
        // Calculate difference
        const resWithWorker = end - start;
        // Send result
        this.postMessage(end - start);
    };
    ```

    **示例:**

    ```
    Output: 'No worker: 5000'
    Output: 'With worker:  5000'

    ```

    这就是没有工作代码时页面的行为方式:

    *   The animation freezes because the JavaScript is blocking the *DOM*.![Complex Calculation Without a Web Worker](img/789766e237f2ac67be3bde3ae88557b8.png)

    没有 webworker 的页面行为

    这就是页面在我们的工作代码中的行为:

    *   正如您所看到的，背景中的动画不会因为我们的工作人员为我们计算而中断。这样，我们让 DOM 线程独立运行。![Complex Calculation with a Web Worker](img/80b026c7e0042a51b4a380a368d1dda2.png)

    网络工作者的页面行为