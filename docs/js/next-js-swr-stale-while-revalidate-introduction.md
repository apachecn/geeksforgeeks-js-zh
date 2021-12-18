# 下一篇 js SWR(重新验证时过时)简介

> 原文:[https://www . geesforgeks . org/next-js-SWR-state-while-revalidate-introduction/](https://www.geeksforgeeks.org/next-js-swr-stale-while-revalidate-introduction/)

**状态同时重新验证**是由 Zeit 创建的远程数据获取的 React Hooks 库。它用于

*   从缓存中返回数据(陈旧)
*   发送提取请求(重新验证)，然后
*   再次提供最新数据。

**谷歌谈及 SWR 的概念:**

> “它帮助开发人员在即时性(立即加载缓存内容)和新鲜性(确保缓存内容的更新在未来使用)之间取得平衡。如果您维护定期更新的第三方 web 服务或库，或者您的第一方资产的生命周期往往很短，那么过时而重新验证可能是对现有缓存策略的有益补充。”

包含过时而重新验证的缓存控制响应头也应该包含最大年龄，通过最大年龄指定的秒数决定了过时。任何比最大年龄新的缓存响应都被认为是新的，旧的缓存响应是陈旧的。简而言之，一旦从缓存中呈现数据，SWR 就会自动重新验证来自源的数据，这将更快地呈现页面，并且在呈现页面后，数据会更新为最新的数据。

**SWR 的优势:**除了自定义 API 调用& REST API 集成外，Zeit 的 SWR 附带的内容描述如下。

*   **焦点重新验证:**当您在浏览器中重新聚焦页面或在选项卡之间切换时，SWR 会自动重新验证数据。
*   **快速导航**:一旦从缓存中渲染数据，SWR 就会自动从原点重新验证数据。
*   **在间隔**上重新预取:SWR 会给你自动获取数据的选项，其中预取只会发生在屏幕上与钩子相关的组件上。
*   **局部突变**:将更改应用于本地数据，即始终更新为最新数据。
*   **依赖取数** : SWR 允许你取数依赖其他数据的数据。它确保了最大可能的并行性(避免瀑布)，以及当下一个数据需要一段动态数据时的串行提取。
*   **可伸缩** : SWR 的伸缩性非常好，因为它只需要很少的努力就能编写出自动并最终收敛到最新远程数据的应用程序。

**SWR 的劣势:**

*   使用 SWR 的一个主要缺点是，它可能会导致用户查看过时的数据，这可能是因为缺少适当的应用编程接口实现、更新显示信息时出错以及其他许多原因。
*   除了造成不好的用户体验，这也可能是一家公司受挫的唯一原因！想象一下，一家在金融领域颇有名气的公司，他们能让用户看到过时的数据吗？？不，这就是为什么需要准确实施和使用 SWR。

**next . js 简介:**

Next.js 是一个基于 react 的框架。正是基于反应过来，**网络包**T2【巴别塔】。它以自动代码拆分、热代码重新加载(即一旦保存更改就重新加载)而闻名&最重要的是服务器端渲染。这将这个框架放在 React 文档中推荐的工具链之上。

考虑到一个节点的设备上安装了& npm，设置您的 **next.js** 项目所采取的步骤。

*   **步骤 1:** 通过运行以下命令

    ```
    $node -v && npm -v
    ```

    检查节点& npm 版本
*   **第二步:**创建目录，到达终端目标目录后执行

    ```
    $ npm install --save next react react-dom
    ```

*   **第三步:**在 pages 文件夹(基本上是 pages/index.js)的 **index.js** 中创建一个文件，添加以下代码，运行 npm start 即可看到它在运行！

## java 描述语言

```
// The code for pages/index.js

import React from'react'; 
import Link from'next/link';

export default class extends React.Component { 
    render() { 
        return ( { 
        <div> 
            <h1>Hello Geeks</h1> 
        </div> 
        ) 
    }   
} 
```

**使用 Next.js 配合 SWR 获取一个 API:**

我们将使用 SWR &与强大的**同构执行数据提取，这是需要安装的两个依赖项(代码中给出的命令)。**

## java 描述语言

```
// The code for /pages/index.js

/* Install by using the CLI - npm i swr */
import useSWR from 'swr'; 

import fetch from '../libs/fetch';

function StateNameAN () {
  const { data, error } = useSWR(
'https://gist.githubusercontent.com/shubhamjain/35ed77154f577295707a/raw/7bc2a915cff003fb1f8ff49c6890576eee4f2f10/IndianStates.json', fetch);
  /* In case API fails */
  if (error) return <div>failed to load</div> 

  /* While result API loads */
  if (!data) return <div>loading...</div> 

  /* After response from the API is received */
  return <div>Hello{' '}{data.AN}!</div> 
}

export default function IndexPage() {
  return (
    <div>
      <StateNameAN />
    </div>
  );
}
```

## java 描述语言

```
// The code for /libs/fetch.js

/* Install by using the CLI - npm i isomorphic-unfetch */
import fetch from 'isomorphic-unfetch'; 

export default async function (...args) {
  const res = await fetch(...args)
  return res.json()
}
```

**输出:**

```
Hello Andaman and Nicobar Islands! 
```