# JavaScript 中选择和选择 2 的区别

> 原文:[https://www . geesforgeks . org/JavaScript 中选择和选择 2 的区别/](https://www.geeksforgeeks.org/difference-between-chosen-and-select2-in-javascript/)

在这个例子中，我们将解释 JavaScript 的**selected**和 **Select2** 插件，并强调两者之间的主要区别。在我们详细讨论这个话题之前，让我们先看看这两个插件。

**selected:**selected 是一个用于 jQuery、Prototype 和 Mootools 的 JavaScript 插件，可以创建又长又大的用户友好的选择框。

**精选的主要特点:**

1.  **用户友好:**不用强迫你的用户在一个巨大的物品列表中滚动，他们只需在他们要找的物品名称上标记星号即可。不匹配的条目将从视图中移除，单击“输入”或鼠标点击就足以选择选项。
2.  **渐进式增强:**selected 消除了为使其适用于没有 JavaScript 的浏览器而做任何特殊工作的麻烦，因为**selected**取代了普通的 HTML **Select** 字段。后端也没有处理数据的事件。
3.  **无痛设置:**selected 自动尊重 opt-group、选中状态、多属性和浏览器选项卡顺序，只需将**selected**文件添加到你的应用程序中并触发插件。

**选择 2:** **选择 2** 被创建来替换浏览器显示的标准**选择**标签。它支持标准选择框中的所有选项和操作，但更具灵活性。**选择 2** 的一些特点是:

*   **可定制:**它为用户提供了可定制的选择框，并支持搜索、标记、远程数据集、无限滚动和许多其他选项。
*   **RTL 环境:**支持 RTL 环境，内置搜索 40 多种语言。
*   **Ajax:** 使用 Ajax 可以高效地搜索大列表项。
*   **CSS:** Fully skinnable, CSS built with **Sass** and an optional theme for Bootstrap 3.

    **选择和选择 2 的区别:**
    选择和选择 2 是扩展选择框的两个最流行的库。两者都是主动维护的，**选择的**比**选择的 2** 旧，同时支持 jQuery 和 Prototype。**选择 2** 只支持 jQuery，选择 2 的灵感来源于**选择的**。

    <figure class="table">

    | **choosed** | **select 2** |
    | Choosed needs to load the whole data set into DOM as an option tag, which limits it to handle only small data sets of class. | Select2 uses the function to dynamically find the results, allowing it to partially load the results. |
    | Since Chosen needs to load the entire data set, paging is not required. | Because Select2 is suitable for large data sets and only loads a few matching results, it must support paging. When the user scrolls to the bottom of the currently loaded results and allows more results to be loaded, Select2 will call the search function. |
    | Choosed only supports rendering text results, because it is the only tag supported by the option tab. | Select2 provides an extension point that can be used to generate any type of tag to represent the result. |
    | Choosed does not support the ability to add results dynamically. | Select2 provides the ability to add results from search terms entered by users, which allows it to be used for tagging. |
    | 挑选是在厚颜无耻和咖啡脚本中开发的。 | Select2 is ordinary CSS and JS. |
    | Size: 27KB | Size: 57KB |
    | There are overflow selection internal elements: hide or overflow: automatic; Does not work in Selected. | Select2 supports this function. |
    | In Chosen, if you have an option called GeeksForGeeks, you have to type Gee… and so on to get the result. | By choosing 2, you can start searching anywhere in the phrase. For example, you can type eek, and you will get the GeeksForGeeks option in the search results because it contains "eek". |

    </figure>

    **注意:**已经发现 Saas 和 CoffeeScript 在 selected 的调试过程中造成的难度要大得多。
    Select2 支持移动，而 Select 在移动平台上明确禁用。因此，如果您想在手机上使用“扩展选择框”，建议使用选择 2。