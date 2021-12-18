# 如何在 Next.js 中添加推文？

> 原文:[https://www.geeksforgeeks.org/how-to-add-tweets-in-next-js/](https://www.geeksforgeeks.org/how-to-add-tweets-in-next-js/)

在本文中，我们将学习如何在 NextJs 中添加推文。NextJS 是一个基于 React 的框架。它有能力为不同的平台开发漂亮的网络应用程序，如视窗、Linux 和 mac。动态路径的链接有助于有条件地呈现您的 NextJS 组件。

**方法:**要添加我们的推文，我们将使用 react-tweet-embed 包。react-tweet-embed 包可以帮助我们在应用程序的任何地方添加 tweet。首先，我们将安装 react-tweet-embed 包，然后我们将在主页上添加一条 tweet。

**创建 NextJS 应用程序:**您可以使用以下命令创建一个新的 NextJs 项目:

```
npx create-next-app gfg
```

**安装所需的包:**现在我们将使用以下命令安装 react-tweet-embed 包:

```
npm i react-tweet-embed
```

**项目结构:**会是这样的。

![](img/5fb51ccebb078290a762cc45f97079de.png)

**添加推文:**我们可以在安装了 react-tweet-embed 包后，在我们的 app 中轻松添加推文。对于这个例子，我们将在主页上添加推文。

在 **index.js** 文件中添加以下内容:

## java 描述语言

```
import TweetEmbed from 'react-tweet-embed'
import React from 'react'

export default function Tweets() {
  return (
    <div>
      <h3>GeeksforGeeks - Tweet</h3>
      <TweetEmbed id='1456503289512710147' 
                  options={{theme: 'dark' }}/>
    </div>
  )
}
```

**说明:**首先在上面的例子中，我们是从已安装的包中导入 TweetEmbed 组件。之后，我们将在我们的 TweetEmbed 组件中添加 id 和 options 参数。你可以在推文链接中找到推文 id。

**运行应用的步骤:**在终端运行下面的命令运行应用。

```
npm run dev
```

### 输出:

![](img/655805087783f19b1e43d5b4c71979c0.png)