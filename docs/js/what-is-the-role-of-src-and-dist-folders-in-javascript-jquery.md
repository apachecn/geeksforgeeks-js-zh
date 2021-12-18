# src 和 dist 文件夹在 JavaScript/jQuery 中的作用是什么？

> 原文:[https://www . geesforgeks . org/什么是-src-and-dist-folders-in-JavaScript-jquery/](https://www.geeksforgeeks.org/what-is-the-role-of-src-and-dist-folders-in-javascript-jquery/)

使用标准的文件夹结构并不是绝对的要求，但是根据 JavaScript/jQuery 社区一直遵循的惯例，强烈建议使用标准的文件夹结构。

一些常见的**目录**有 **lib/** 、 **src/** 、 **build/** 、 **dist/** 、 **bin/** 、 **test/** 、 **unit/** 、 **integration/** 、 **env/**

**src:** 它代表源代码，是在缩小、拼接或其他编译之前的原始代码，用于读取或编辑代码。

```
src/
```

1.  [T0】 src 【T1] stands for **source** .
2.  The [T0】 /src 【T1] folder contains the original unrefined code.
3.  The [T0】 /src 【T1] folder is used to store files, and its main purpose is to read (and/or edit) codes.
4.  The [T0】 /src 【T1] folder contains all sources, that is, codes that need to be operated before use.
5.  Depending on the project, the **/src** folder may contain only pure source code or non-condensed version.
6.  Therefore, the **/src** folder is mainly used to store any source code files before reduction.

**dist:** 它代表分销，是生产现场实际使用的缩小或串联版本。

```
dist/
```

1.  [T0】 /dist 【T1] stands for **distributable** .
2.  The /dist folder contains the minimized version of the source code.
3.  The code that appears in the /dist folder is actually the code used in the production web application.
4.  In addition to the streamlined code, the /dist folder also contains all compiled modules, which may or may not be used in other systems.
5.  It is easier to add files to the /dist folder because it is an automatic process. When saving, all files are automatically copied to the dist folder.
6.  The /dist folder also contains all the files needed to run/build modules for other platforms-either directly in the browser or in AMD system (such as require.js).
7.  Ideally, it is considered a good practice to clean up the /dist folder before each build.

**示例:**任何程序或库的源代码都存在于/src 目录中。现在，如果一个人希望使用某个库(C、C++、Java 等)的源代码。)是另一个人写的，那么他们需要先编译源代码，然后才能使用它。如果这个源代码不符合，那么就不可能使用它们。然而，如果源代码的预编译版本已经可用，那么就不需要完成编译源代码文件的任务，可以直接使用。这样一个已经编译的版本被保存到/dist 目录中。

同样，如果希望共享一个 JavaScript 库，应该将原始(未缩小)源代码添加到 src/文件夹中，将缩小(预编译)版本添加到 dist 文件夹中。通过这样做，任何人都可以立即使用代码的缩小版本，而不必自己缩小它。