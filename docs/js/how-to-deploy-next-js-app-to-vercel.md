# 如何将 Next.js App 部署到 Vercel？

> 原文:[https://www . geesforgeks . org/如何部署-下一个-js-app-to-vercel/](https://www.geeksforgeeks.org/how-to-deploy-next-js-app-to-vercel/)

**简介:** Vercel 是前端开发人员使用的部署工具，无需了解复杂的配置即可即时部署和托管 web 应用。

#### Vercel 的特点:

*   易于使用，并有一个终身免费的层服务，这是有益的初学者谁想要部署他们的边项目与最少的支持。
*   可以使用 GitHub、GitLab、Bitbucket 或电子邮件创建帐户。
*   允许开发人员使用启用了 HTTPS 的自定义域。
*   可以用来建立无限的网站和 API。
*   数据的变化导致网页的自动推送，从而减少静态生成的约束。
*   高性能边缘网络可加快路由速度。
*   每个拉取请求都有它的预览网址，这在运行测试或收集反馈时很有用。

**步骤 1:创建 Next.js 应用程序并设置 Vercel 帐户:**通过运行以下命令创建 Next.js 应用程序:

```
npx    create-next-app
```

或者

```
yarn create next-app     
```

一旦 Next.js 应用程序被创建，转到 Vercel 网站并注册 GitHub/Email-id 来创建一个帐户。为了部署我们的应用程序，我们需要安装 Vercel 命令行界面。运行以下命令以全局安装 Vercel(您也可以在项目文件夹中本地安装 Vercel)。

```
npm i -g vercel
```

要检查 vercel 是否安装在我们的机器上，运行命令:

```
vercel --version
```

如果 vercel 安装正确，它将安装最新版本，即 **23.0.0**

通过运行以下命令

```
vercel login
```

登录您的 vercel 帐户

系统将提示您以下问题–输入您的电子邮件:输入您的邮件进行确认。

**第二步:部署:**登录后，为了部署您的 Next.js 项目，您需要运行**‘vercel’**命令。

```
vercel
```

该命令将显示最新的 Vercel 版本，并询问以下问题:

1.  And deploy "~/projectname"? [Yes/No]:
2.  What scope do you want to deploy to?
3.  Link to existing project? 【y/n】
4.  What is the name of your project?
5.  What directory is your code located in?
6.  Do you want to overwrite the settings? 【y/n】

完成这些问题后，前往您的 Vercel 帐户，点击**访问**按钮，在 Vercel 上观看您的项目直播。

**注意:**从命令行部署项目后，Vercel 会创建一个包含 **project.json** 文件的. **vercel** 文件夹。该文件包含**原始**和**项目标识**密钥，这些密钥是机密的，**“不应”**被推送到 Git。

**步骤 3(可选):使用 Git 和 GitHub 实现自动化:** Vercel 会自动部署对 Git 存储库所做的任何更改。每次创建新的拉或合并请求时，Vercel 都会创建新的构建并设置新的部署。