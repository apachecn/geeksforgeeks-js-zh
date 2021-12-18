# 如何在 JavaScript 中链接异步函数？

> 原文:[https://www . geesforgeks . org/how-to-chain-asynchronous-in-JavaScript/](https://www.geeksforgeeks.org/how-to-chain-asynchronous-functions-in-javascript/)

JavaScript 是*单线程* *异步*函数是一个耗时的操作，可以在不阻塞线程其他操作的情况下执行。这可以通过异步代码来实现，如[**承诺**](https://www.geeksforgeeks.org/javascript-promises/) 或 [**异步**](https://www.geeksforgeeks.org/understanding-the-async-in-javascript/) 功能(基本上是更干净的承诺)。异步函数很酷，但是它们的执行时间不确定，这有时会产生问题，当我们有两个相互依赖的**异步**函数时。

**注:**本文将使用 ES2015+功能，如**异步**功能、箭头功能等。但是，使用旧的 ES 功能也可以获得相同的结果。

**示例 1:** 为了帮助我们，我们有三个**异步**函数(黑盒函数)。

## Javascript

```
<script>
  async function getUserData() {
      console.log('Fetching data');     
  }

  async function cleanUserData(userData) {
      console.log('Cleaning data');      
  }

  async function saveToDataBase(userData) {
      console.log('Saving to DB');     
  }
  const userData = getUserData();
  const cleanedData = cleanUserData(userData);
  saveToDataBase(cleanedData);
</script>
```