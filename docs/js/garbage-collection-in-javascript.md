# JavaScript 中的垃圾收集

> 原文:[https://www . geesforgeks . org/垃圾收集-in-javascript/](https://www.geeksforgeeks.org/garbage-collection-in-javascript/)

本文将解释 JavaScript 中垃圾收集的概念。要了解垃圾收集的需求，首先要了解**内存生命周期**

**内存生命周期:**内存生命周期对于任何编程语言来说都差不多，它有 3 个主要步骤。

*   分配内存。
*   使用分配的内存进行读取或写入，或者两者都使用。
*   当不再需要时，释放分配的内存。

**垃圾收集背后的概述:**大多数内存管理问题发生在我们试图释放分配的内存时。出现的主要问题是确定未使用的内存资源。在开发人员必须手动决定何时不再需要内存的低级语言中，高级语言如 **JavaScript** 使用一种称为**垃圾收集(GC)的自动化内存管理形式。**

**垃圾收集:**下一节将解释理解主要垃圾收集算法所需的概念及其局限性。为垃圾收集设计的算法的主要概念是 ***参考*** 的概念。如果*前一个对象可以访问后者*，则一个对象可以引用另一个对象。例如，一个 JavaScript 对象可以有一个隐式引用(当引用指向它的原型时)和一个显式引用(当引用指向它的属性值时)。
下面我们将解释用于垃圾收集的算法。

1.  **引用计数垃圾收集:**该算法被认为是最基本的一类垃圾收集算法。这些算法的作用是，它不是确定任何资源是否重要，而是扫描内存来确定一个对象是否有任何其他对象引用它。具有**零**引用的对象被认为是**垃圾**或“可收集的”。

    **示例:**

    ## java 描述语言

    ```
    // Consider the following example

    // Declare an object
    var object_1 = {
        object_2: {
            object_3: 7
        }
    };

    // In this example, create two objects
    // One object is referred by another 
    // as one of its properties. Currently, 
    // none can be garbage collected

    // The "object_4" variable is the second
    // thing that has a reference to the object
    var object_4 = object_1;

    // The object that was originally in 
    // "object_1" has a unique reference 
    // embodied by the "object_4" variable
    object_1 = 1;

    //Reference to "object_2" property of
    // the object. This object now has 2 
    // references: 1 as a property,
    // The other as the "object_5" variable.
    var object_5 = object_4.object_2;

    // The object that was in "object_1" has
    // now zero references to it. It can be 
    // garbage-collected. However its "object_2"
    // property is still  referenced by the
    // "object_5" variable, so it cannot be freed.
    object_4 = "Geeks For Geeks";

    // Now the "object_2" property has no 
    // references to it and hence it can
    // be garbage collected.
    object_5 = null;
    ```

    #### 障碍物:圆形参照

    当涉及到循环引用时，限制就出现了。当使用相互引用的属性创建两个对象时，会出现循环引用，从而创建一个循环。
    引用计数算法无法回收这些内存资源，因为每个对象至少有一个引用指向它们，这防止了两个对象都被标记为垃圾收集。循环引用是内存泄漏的主要原因之一。
    以下示例显示了所述情况的一个实例。

    **示例:**

    ## java 描述语言

    ```
    function Demo() {
        var one = {};
        var two = {};

        // one reference to two
        one.object = two;

        // two reference to one
        two.object = one;

        return 'circular';
    }

    Demo();
    ```

2.  **Mark-and-sweep-algorithm:** This algorithm modifies the problem statement from the “object being no longer needed” to the object being “unreachable”. This algorithm demands a prerequisite of the knowledge of **roots** which are a set of objects. In JavaScript, a root is a global object. On a regular basis, the garbage collector starts from these roots and finds all the objects that are referenced from these roots, then all objects referenced from these, etc. Starting from the roots, the garbage collector will find all the objects that are reachable and mark all the non-reachable objects.

    **周期不再是问题:**函数调用返回后，这两个对象不再被从根或全局对象可达的任何资源引用。因此，这些将被垃圾收集器标记为**不可达**，并回收其分配的内存。

    **一些限制:**唯一可以发现的限制是，在 JavaScript 中无法显式或编程地触发垃圾收集器。
    因此，如果在某些情况下可以方便地手动编程何时释放内存，那么 JavaScript 中就没有触发这种事件的规定。