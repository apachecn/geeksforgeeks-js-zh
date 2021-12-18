# 如何使用 JavaScript 自动喜欢 facebook 新闻提要上的多个帖子？

> 原文:[https://www . geesforgeks . org/how-like-multi-post-on-Facebook-news-feed-automatic-use-JavaScript/](https://www.geeksforgeeks.org/how-to-like-multiple-posts-on-facebook-news-feed-automatically-using-javascript/)

在本文中，我们将学习如何在脸书新闻提要上自动喜欢多个帖子。很多时候，我们浪费了太多的时间去喜欢我们新闻提要中的所有帖子。因此，这个脚本将有助于通过自动化这个任务来减少我们的时间和精力。

**进场:**

1.  制作一个变量帖子，指向当前页面上所有帖子的数组。
2.  运行一个循环来迭代所有的帖子。
3.  现在我们检查一下这个帖子是否还没有被喜欢。
4.  然后点击那个帖子的相似按钮。

**以下是步骤:**

*   使用**m.facebook.com**进入脸书页面
*   登录并打开新闻源/主页。
*   在 Chrome 中按 Ctrl+Shift+I 打开开发者模式
*   导航到控制台。
*   现在，运行下面的脚本。
    **例:**

```
var posts = document.getElementsByClassName("_15ko");
for(var i=0;i<posts.length;i++)
{
    if(posts[i].classList.contains("_77la")==false)
    {
        posts[i].click();
    }
}
```

**输出:**

![](img/e082bc339ca2996ae76fdeb859697e94.png)

输出

**注意:**请确保有稳定的互联网连接可用，以便脚本顺利运行。还要确保使用**m.facebook.com**而不是**www.facebook.com**访问 facebook，因为此脚本仅适用于移动版 facebook。

> 本教程仅用于教育目的，请不要用它来打扰任何人或任何不道德的方式。