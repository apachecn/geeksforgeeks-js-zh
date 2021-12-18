# p5.js |队列中的出列操作

> 原文:[https://www . geesforgeks . org/P5-js-出列-排队操作/](https://www.geeksforgeeks.org/p5-js-dequeue-operation-in-queue/)

**什么是队列？**
队列是一种线性结构，它遵循执行操作的特定顺序。顺序是先进先出。队列的一个很好的例子是资源的任何消费者队列，其中先到的消费者先被服务。在队列中添加或移除元素需要恒定的时间。当我们需要处理**先进先出**形式的数据时，应该在数组上使用
![queue](img/a3f253b1dbe832f1e2665a79f5b25dc9.png)
队列。

**队列中的出列操作:**在队列中，访问内容的同时将其从队列的前端移除，称为**出列**操作。
![](img/6e7b1829ffc4ae48a8947e6588625d6a.png)

**方法:**出列操作可能包括以下步骤:

*   检查队列是否为空。如果队列是空的，那么它会产生一个错误并退出。
*   如果队列不为空，则访问前端指向的数据元素。
*   使用 array.pop()操作删除缓冲区中的元素。
*   回报成功。

**示例 1:** 本示例实现了入队操作来创建队列。

```
<!DOCTYPE html>
<html>

<head>
    <title>Dequeue Operation in Queue</title>

    <meta charset="UTF-8">

    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"
    type="text/javascript"></script>

    <style> 
        body {
            padding: 0;
            margin: 0;
        } 
        canvas {
            vertical-align: top;
        }
    </style>
</head>

<body>    
    <script>

        // Define Queue function 
        function Queue(array) {
            this.array = [];
            if (array) this.array = array;
        }

        // Add Get Buffer property to object constructor
        // which slices the array
        Queue.prototype.getBuffer = function() {
            return this.array.slice();
        }

        // Add isEmpty properties to object constructor which
        // returns the length of the array
        Queue.prototype.isEmpty = function() {
            return this.array.length == 0;
        }

        // Instance of the Queue class
        var queue1 = new Queue(); // Queue { array: [] }

        console.log(queue1);

        // Add Push property to object constructor 
        // which push elements to the array
        Queue.prototype.enqueue = function(value) {
            this.array.push(value);
        }

        function setup() {

            // Create Canvas of size display width * 300
            createCanvas(displayWidth, 300);
        }

        function draw() {

            // Set background color
            background("grey");

            // Set stroke weight
            strokeWeight(3);
            textAlign(CENTER);
            textSize(24);
            text("Queue Implementation Using P5.js",
                        windowWidth/2, 20);
            textAlign(LEFT);
            textSize(14);

            // Set stroke color
            stroke('green');
            line(10, 45, 90, 45);
            rect(10, 30, 60, 30);
            noStroke();
            text("FRONT", 20, 50);

            // Display queue
            for(var i = 0; i <= queue1['array'].length-1; i++) {
                var p = 10;
                translate(70, 0);
                strokeWeight(3);
                stroke('green');
                line(10+p, 45, p+80, 45);

                rect(10+p, 30, 40+p, 30);
                noStroke();
                text(queue1['array'][i], 40, 50);
                p += 10;
            }

            // Set stroke color
            stroke('green');
            translate(70, 0);
            rect(10, 30, 60, 30);
            noStroke();
            text("REAR", 20, 50);
        }

        // Peek Function
        Queue.prototype.peek = function() {
            return this.array[this.array.length-1];
        }

        // Driver Code
        // Call to Enqueue operation
        queue1.enqueue(1);
        queue1.enqueue(2);
        queue1.enqueue(3);
        queue1.enqueue(19);
        queue1.enqueue(11);
        queue1.enqueue(15);
        queue1.enqueue(14);
        queue1.enqueue(18);
        queue1.enqueue(25);
    </script>
</body>

</html>                              
```

**输出:**
![](img/aedb035e7f86031eb68d16b40b69aa9b.png)

通过调用 *queue1 .出列()*函数执行两次出列操作后，前值变为 3。

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>Dequeue Operation in Queue</title>

    <meta charset="UTF-8">

    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.8.0/p5.min.js"
    type="text/javascript"></script>

    <style> 
        body {
            padding: 0;
            margin: 0;
        } 
        canvas {
            vertical-align: top;
        }
    </style>
</head>

<body>    
    <script>

        // Define Queue function 
        function Queue(array) {
            this.array = [];
            if (array) this.array = array;
        }

        // Add Get Buffer property to object constructor
        // which slices the array
        Queue.prototype.getBuffer = function() {
            return this.array.slice();
        }

        // Add isEmpty properties to object constructor which
        // returns the length of the array
        Queue.prototype.isEmpty = function() {
            return this.array.length == 0;
        }

        // Instance of the Queue class
        var queue1 = new Queue(); // Queue { array: [] }

        console.log(queue1);

        // Add Push property to object constructor 
        // which push elements to the array
        Queue.prototype.enqueue = function(value) {
            this.array.push(value);
        }

        function setup() {

            // Create Canvas of size display width * 300
            createCanvas(displayWidth, 300);
        }

        function draw() {

            // Set background color
            background("grey");

            // Set stroke weight
            strokeWeight(3);
            textAlign(CENTER);
            textSize(24);
            text("Queue Implementation Using P5.js",
                        windowWidth/2, 20);
            textAlign(LEFT);
            textSize(14);

            // Set stroke color
            stroke('green');
            line(10, 45, 90, 45);
            rect(10, 30, 60, 30);
            noStroke();
            text("FRONT", 20, 50);

            // Display queue
            for(var i = 0; i <= queue1['array'].length-1; i++) {
                var p = 10;
                translate(70, 0);
                strokeWeight(3);
                stroke('green');
                line(10+p, 45, p+80, 45);

                rect(10+p, 30, 40+p, 30);
                noStroke();
                text(queue1['array'][i], 40, 50);
                p += 10;
            }

            // Set stroke color
            stroke('green');
            translate(70, 0);
            rect(10, 30, 60, 30);
            noStroke();
            text("REAR", 20, 50);
        }

        // Dequeue function
        Queue.prototype.dequeue = function() {
            return this.array.shift();
        }

        // Peek Function
        Queue.prototype.peek = function() {
            return this.array[this.array.length-1];
        }

        // Driver Code
        // Call to Enqueue operation
        queue1.enqueue(1);
        queue1.enqueue(2);
        queue1.enqueue(3);
        queue1.enqueue(19);
        queue1.enqueue(11);
        queue1.enqueue(15);
        queue1.enqueue(14);
        queue1.enqueue(18);
        queue1.enqueue(25);

        // Call to Dequeue Function
        queue1.dequeue();
        queue1.dequeue();
    </script>
</body>

</html>                        
```

**输出:**
![](img/458f86f1720384b1bd5840a6c172dcc6.png)