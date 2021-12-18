# JavaScript | promise . all settled()方法

> 原文:[https://www . geesforgeks . org/JavaScript-promise-all settled-method/](https://www.geeksforgeeks.org/javascript-promise-allsettled-method/)

JavaScript 中的[](https://www.geeksforgeeks.org/javascript-promises/)**承诺可以处于待定、履行或拒绝三种状态。Javascript 中的 **Promise.allSettled()** 方法用于在所有输入都已完成或被拒绝时获得一个承诺。**

****语法:****

```
Promise.allSettled(iterable);
```

****参数:**该方法接受单个参数**可迭代**，该参数取一个*承诺的数组*或一个包含一些对象的普通数组。**

****返回值:**该方法返回以下值:**

*   **如果传递的参数为空，则返回一个已经*解析*的承诺。**
*   **对于所有其他情况，它返回一个**待定**承诺。**

****例 1:****

## **java 描述语言**

```
<script>
    // Illustration of Promise.allSettled()
    // Method in Javascript with Example

    const p1 = Promise.resolve(50);
    const p2 = new Promise((resolve, reject) =>
                    setTimeout(reject, 100, 'geek'));
    const prm = [p1, p2];

    Promise.allSettled(prm).
      then((results) => results.forEach((result) =>
      console.log(result.status,result.value)));
</script>
```

 ****输出:****

```
"fulfilled"
 50
"rejected" 
 undefined
```

****例 2:****

## **java 描述语言**

```
<script>
    // Simple promise that resolves
    // After a given time
    const tOut = (t) => {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve(`Completed in ${t}`)
        }, t)
      })
    }

    // Resolving a normal promise
    tOut(1000).then(result => console.log(result)) 
    // Completed in 1000

    // Promise.allSettled
    Promise.allSettled([tOut(1000), tOut(2000)]).then(result =>
    console.log(result))
</script>
```

****输出:****

```
"Completed in 1000"
Array [Object { status: "fulfilled", value: "Completed in 1000" }, 
Object { status: "fulfilled", value: "Completed in 2000" }]
```

****支持的浏览器:****

*   **谷歌 Chrome 6.0 及以上版本**
*   **Internet Explorer 9.0 及以上版本**
*   **Mozilla 4.0 及以上版本**
*   **Opera 11.1 及以上**
*   **Safari 5.0 及以上版本**