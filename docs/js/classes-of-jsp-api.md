# JSP API 的类

> 原文:[https://www.geeksforgeeks.org/classes-of-jsp-api/](https://www.geeksforgeeks.org/classes-of-jsp-api/)

JSP API 是一组可以用来制作 JSP 页面的类和接口。这些类和接口包含在 javax servlet.jsp 包中。javax 中描述的一部分类。servlet.jsp 套餐有:

1.  错误数据
2.  JSP 编写器
3.  页面上下文

**错误数据类:**错误信息类表征错误页面的错误数据。您必须设置页面要求的估计值，*iserrrpage*以与证明页面是错误页面保持一致。错误信息类扩展了 *java.lang.Object 类*。可以在 JSP 页面中使用的错误数据中描述的部分策略是:

1.  **getRequestURL():** 通过 String 返回提到的 URL。
2.  **getServletName():** 返回通过 String 调用的 servlet 的名称。
3.  **getStatusCode():** 以整数形式返回失策的状态码。
4.  **getThrowable():** 返回导致错误的可抛出特例。

**JspWriter 类:**在 JSP 页面中，为了组合活动和布局信息，我们可以利用 JspWriter 类。理解的变量给出了 JSPWriter 类对象。JSPWriter 类扩展了 java.io.Writer 类。JSP 页面中可以使用的 JSPWriter 类中的一部分技术是:

1.  **清除():**清除摇篮的物质。如果支持现在被清除，合理()技术抛出一个 IOException 特例。
2.  **关闭():**关闭并冲洗水流。
3.  **冲洗():**冲洗摇篮流。flush()策略会刷新一系列写入器和输出流中的每个托架。它抛出 java.io.IOException 特例，以防在关闭流后调用 compose()或 flush()。
4.  **getBufferSize():** 返回 JSPWriter 使用的支持的大小。
5.  **print():** 打印排序布尔、整数、字符、长整数、滑动点、双倍精度滑动点数字、各种字符、字符串和项目的估计值。print()抛出 java.io.IOException，如果在打印时出现任何错误。
6.  **println():** 打印排序布尔值、整数、字符、长整数、漂移点、双倍精度滑动点数字、各种字符、字符串和文章的估计值。Println()抛出 java.io.IOException，如果在打印时出现任何错误。

**页面上下文类:**在 servlet 条件下利用 JSP 创新时，设置数据由页面上下文类给出。PageContext 类扩展了 JSPContext 类。页面上下文提供了对与 JSP 页面相关的名称空间的访问。页面上下文类中描述的一些策略是:

1.  **forward():** 将当前 servlet 需求和 servlet 反应重定向到另一个页面。这种策略将目标页面的网址视为一种竞争。
2.  **getPage():** 返回页面对象的当前估计。
3.  **getRequest():** 返回征集对象的当前预估值。servlet 请求是 getRequest()的到达类型。
4.  **getResponse():** 返回反应对象的当前估计。getResponse()技术的返回类型是 servlet 反应。
5.  **getServletConfig():** 返回当前页面的 ServletConfig。
6.  **getServletContext():** 返回当前页面的 ServletContext。
7.  **getSession():**getSession()的到达种类是 HttpSession。它将恢复当前页面上下文。
8.  **include():** Processes the current servlet demand and the reaction determined in the URL. The incorporate() technique accepts two contentions, a URL way and the flush estimation of boolean sort.

    **JSP 中的会话跟踪:**

*   **Cookies:** 放在客户机器上的一个小消息字段。治疗可能会在程序设置中受到损害，因此无法经常访问。
*   **网址改造:**在网址中存储会话数据。当 treats 还没有得到支持时，Works 可能会使网站页面的书签成为一个问题，因为它们在网址结束时有会话显式数据。
*   **避免的字段:** HTML 掩盖了变更框，例如:

```
<input type = "hidden">
```

*   **会话对象:** JSP 隐式对象。会话文章利用密钥/尊重组合来存储信息。从会话中检索数据:

```
session.getValued("msg") 
```

*   getValue 策略的到达类型是 Object，因此您应该键入 case 来获得所需的值。当会话名称中没有这样的密钥时，将返回无效。