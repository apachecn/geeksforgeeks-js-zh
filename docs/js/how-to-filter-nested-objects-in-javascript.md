# 如何过滤 JavaScript 中的嵌套对象？

> 原文:[https://www . geesforgeks . org/如何过滤 javascript 中的嵌套对象/](https://www.geeksforgeeks.org/how-to-filter-nested-objects-in-javascript/)

**filter()** 方法创建一个新数组，其中所有元素都通过了由提供的函数实现的测试。

**方法 1:** 该方法使用 filter()方法过滤 JavaScript 中的嵌套对象。

**示例:**

## HTML

```html
<!DOCTYPE html>
<html>

<body>
    <h2>Output</h2>
    <p id="Output"></p>

    <script>
        var nestedObject = [
            {
                itemId: 1,
                itemDetails: {
                    name: "C",
                    caregory: "Programming Language",
                    price: 500,
                },
                itemCategory: "Basic",
            },
            {
                itemId: 2,
                itemDetails: {
                    name: "C++",
                    caregory: "Programming Language",
                    price: 700,
                },
                itemCategory: "Beginner",
            },
            {
                itemId: 1,
                itemDetails: {
                    name: "Java Script",
                    caregory: "Web Development",
                    price: 1500,
                },
                itemCategory: "Advanced",
            }]
        let itemNames = nestedObject.filter(
            eachObj => eachObj.itemDetails.price === 1500);

        document.getElementById("Output").innerHTML
            = JSON.stringify(itemNames);
    </script>
</body>

</html>
```