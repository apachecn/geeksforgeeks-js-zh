# JavaScript |代理()对象

> 原文:[https://www.geeksforgeeks.org/javascript-proxy-object/](https://www.geeksforgeeks.org/javascript-proxy-object/)

JavaScript 中的代理对象用于定义基本操作(例如，属性查找、赋值、枚举、函数调用等)的自定义行为。

**语法:**

```
var p = new Proxy(target, handler);
```

**参数:**代理对象接受两个参数，如上所述，如下所述:

*   **Target:** The target object (which can be any type of object, including functions, classes, or even another agent) is wrapped with an agent.
*   **Handler:** An object whose attribute is a function that defines the behavior of the agent when it performs operations on it.

**例:**

```
                        <script>
const Person = {
    Name: 'John Nash',
    Age: 25
};

const handler = {
    // target represents the Person while prop represents
        // proxy property.
    get: function(target, prop) {
        if (prop === 'FirstName') {
            return target.Name.split(' ')[0];
        }
        if (prop === 'LastName') {
            return target.Name.split(' ').pop();
        }
        else {
            return Reflect.get(target,prop);
        }
    }
};

const proxy1 = new Proxy(Person, handler);

document.write(proxy1 + "<br>");

// Though there is no Property as FirstName and LastName, 
// still we get them as if they were property not function.
document.write(proxy1.FirstName + "<br>");
document.write(proxy1.LastName  + "<br>");     
</script>                    
```

**输出:**

```
[object Object]
John
Nash

```

**注意:**以上代码只要安装了 NodeJs 就可以直接在终端运行，否则通过在 script 标签中粘贴上述内容在 HTML 文件中运行，并在任何 web 浏览器的控制台中检查输出。