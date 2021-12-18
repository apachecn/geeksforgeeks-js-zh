# JavaScript 架构流量组件

> 原文:[https://www . geesforgeks . org/JavaScript-架构-通量-组件/](https://www.geeksforgeeks.org/javascript-architecture-flux-components/)

**Flux:** 它是一个 JavaScript 架构或 UI 模式，运行在单向数据流上，有一个集中式调度器。这是一种应用程序架构，旨在构建客户端 web 应用程序。它也是脸书用于构建客户端 web 应用程序的流行架构之一。通量体系结构基于以下组件。

**Flux 的四个主要组件:**

1.  **Dispatcher:** It coordinates actions and updates stores.
2.  **Stores:** It serves as a container of app state and logic.
3.  **Actions:** It enables data to be passed to the scheduler.
4.  **View:** It is the same as the view in MVC architecture, but in the context of React component.

简单地说，如果我们理解整体，那么在 Flux 架构中，基本上假设用户点击了某个东西，视图会创建动作；Actions 创建一个新的数据并将其发送给 dispatcher，这里是 dispatcher 的工作，dispatcher 将操作结果调度到适当的存储中。然后，商店根据结果更新状态，并向视图发送更新。

流量应用程序中的数据是单向流动的，或者我们可以说流量应用程序中的数据是单向流动的，单向流动的意义在于，由于数据是单向流经您的应用程序，因此我们可以更好地控制它。

**流程:**

```
Action => Dispatcher => Store => View
```

### **调度员:**

调度程序是管理流量应用程序中所有数据流的中心枢纽，本质上是一个没有自己智能的存储回调注册表，或者我们可以说它是一个将动作分发到存储的简单机制。

*   It is the center of data flow in any Flux application
*   It controls what flows into the Flux application's storage.
*   It serves as a repository for callbacks created by stores and linked to dispatchers.
*   Each store in the application creates a callback and registers it in the scheduler.
*   When an action creator sends a new action to the dispatcher, the dispatcher ensures that all registered stores get the action due to the callback provided.

**注意:**调度器是数据依赖关系的最终仲裁者。

Flux 架构有助于包括使代码更清晰、更新其他视图和由新开发人员进行调试等效果的操作。它还包括一个单独的调度器，所有的动作都通过调度器传递。这种设计保护了难以调试的级联更新。

### **门店:**

存储是应用程序状态和逻辑的中心，角色类似于传统 MVC 中的模型。它向调度程序注册自己，并向它提供一个回调，这个回调接收作为参数的动作。

*   Contains the logic and state of Flux application.
*   The storage in Flux can actually represent the management state of many objects, instead of representing a single data structure like the traditional model.
*   It registers with the scheduler and provides it with a callback.
*   Callback is passed to a parameter called action, which is passed to it through the scheduler.

**注意:**门店是状态居住的地方，只有门店本身才能改变这种状态。

Flux 架构使用存储来缓存与数据或状态相关联的任何应用程序。它包括多个商店。它还具有逻辑处理能力和灵活性，可以决定公开显示数据的哪些部分。

### **动作:**

当 dispatcher 公开了一个方法，允许我们触发对存储的调度，并包含一个有效载荷的数据，我们称之为动作。动作也可以来自其他地方，例如服务器，例如在初始化期间键入数据，或者当服务器返回错误代码，或者当服务器有更新要提供给应用程序时。

*   Actions define methods that the view will call.
*   Is the data form that has been sent to the store.
*   These methods contain parameters that contain further instructions about how the view wants to change the store.
*   Action is responsible for translating dispatch calls into events; This is understandable by the store.

**注:**如果不是动作，就不可能发生。

Flux 体系结构中的操作是方法的集合，这些方法在视图内或视图内部被调用，以向调度程序发送操作。它是通过调度程序交付的实际有效载荷之一。动作类型示例类型集用于定义必须发生什么动作，并与动作数据一起发送。

### **视图:**

这不是 Flux 的技术部分，但同时，视图显然是我们应用程序的关键部分。它通常被理解为我们架构中负责向用户显示数据的部分，是我们数据流架构的最后一站。视图存在于通量之外，但受到通量的单向特性的约束。

*   Simply put, it is the composition of ingredients.
*   It is the part of the architecture that is responsible for displaying data to users.
*   The view layer is the layer that React is suitable for this architecture.

**注意:**数据流出视图的唯一方式是调度一个动作。

它基本上只是一个 React Components，它监听变更事件并从存储中检索应用程序的状态，从而将数据传递给它们的子组件。