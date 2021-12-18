# D3.js 中断()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-interrupt-function/](https://www.geeksforgeeks.org/d3-js-interrupt-function/)

**D3.js** 中的 **d3.interrupt()** 功能用于中断指定节点上指定名称的活动转换，并取消任何具有指定名称的未决转换。该功能类似于**选择.中断()**功能。

**语法:**

```
d3.interrupt(node[, name])

```

**参数:**该功能接受如下参数，如上所述，如下所述:

*   **名称:**此参数为过渡实例。
*   **节点:**该参数是传递参数的节点。

**返回值:**该函数返回中断的活动转换。

以下程序说明了 **D3.js.** 中的 **d3.interrupt()** 功能

**例 1:**

```
<!DOCTYPE html> 
<html> 
<head> 
    <meta charset="utf-8">
    <script src="https://d3js.org/d3.v5.min.js"> 
    </script>
</head> 

<body> 
    <center>
        <h1 style="color: green;"> 
            Geeksforgeeks 
        </h1> 

        <h3>D3.js | d3.interrupt() Function</h3>

        <svg width="400" height="250"></svg>

        <script>
            var svg = d3.select("svg")

            var circle = svg.selectAll("circle")
                .data([1, 2, 3, 4])
                .enter()
                .append("circle")
                .style("fill", "red")
                .attr("cx", 50)
                .attr("cy", function(d) {
                    return d * 50
                })
                .attr("r", 25)
                .on("click", function() {
                    d3.interrupt(d3.select(this))
                })

            circle.transition()
                .delay(function(d) {
                    return d * 500;
                })
                .duration(function(d) {
                    return d * 1000;
                })
                .attr("cx", 360)
                .on("interrupt", function() {
                    var elem = this;
                    var targetValue = d3.active(this)
                    .attrTween("cx")                  
                    .call(this)(1);
                    d3.select(this).attr("cx", targetValue)
                })
        </script> 
    </center>
</body> 
</html>
```

**输出:**

![](img/c369881908660451a4c7dd5e3b962de0.png)

**例 2:**

```
<!DOCTYPE html> 
<html> 
<head> 
    <meta charset="utf-8">
    <script src="https://d3js.org/d3.v5.min.js"> 
    </script>

    <style>
        svg {
          background-color: green;
          display: block;
        };
    </style>
</head> 

<body> 
    <center>
        <h1 style="color: green;"> 
            Geeksforgeeks 
        </h1> 

        <h3>D3.js | d3.interrupt() Function</h3>

        <button>Stop</button>
        <svg width="500" height="150"></svg>

        <script>
            const svg = d3.select("svg");
            const local = d3.local();
            const button = d3.select("button");
            const circle = svg.append("circle")
                .attr("r", 25)
                .attr("cx", 30)
                .attr("cy", 75)
                .style("fill", "yellow")
                .style("stroke", "black");

            circle.transition()
                .delay(5000)
                .duration(10000)
                .ease(d3.easeLinear)
                .attr("cx", 580)
                .on("interrupt", function() {
                    local.set(this, +d3.select(this)
                    .attr("cx"))
                });

            button.on("click", function() {
                if (d3.active(circle.node())) {
                    d3.interrupt(circle);
                    this.textContent = "Resume";
                } 
                else {
                    circle.transition()
                    .ease(d3.easeLinear)
                    .duration(function() {
                        return 10000 * (560 -
                        local.get(this)) / 560;
                    })
                    .attr("cx", 580)
                    this.textContent = "Stop";
                }
            })
        </script> 
    </center>
</body>  
</html>
```

**输出:**

![](img/98eb86525af09024ddee3c03d6ff74a0.png)