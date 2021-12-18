# tensorflow . js TF . data . csvdata set 类

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-data-csvdataset-class/](https://www.geeksforgeeks.org/tensorflow-js-tf-data-csvdataset-class/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

Tensorflow.js 有一套丰富的库，这些库在创建、开发和部署模型方面有很多用途，但是训练或创建模型所需的主要元素是数据。开发和训练一个模型所需的数据通常是巨大的，通常被当作 CSV 文件。因此，TensorFlow Library 提供了一个名为 **CSVDataset** 类的库来处理 CSV 文件。这个 **tf.data.CSVDataset** 类扩展了 **tf.data.Dataset** 类。

**语法:**

```
tf.data.csv( source )
```

**方法:****TF . data . csvdataset**类有一个预定义的方法，叫做 **columnNames()** 函数，帮助获取 CSV 文件的列名。每当数据中有列时，就使用 **columnNames()** 函数进行检索，否则当文件没有列名时会引发错误。可以解析为数字的值作为类型号发出，其他值作为字符串解析。

**语法:**

```
tf.data.csv( source ).columnNames()
```

**参数:**该方法有一个参数，如上所述，如下所述。

*   **Source:** The source is the file where the CSV file is located. It can be a link to a file or a file location in the system.

**返回值:**以数组形式返回 CSV 文件的列名。

**例 1:** 考虑以下 CSV 文件

```
S No., UserName, Address, Mobile number, Item Ordered, Payment Type
1, Bertram, 59 Oak Valley St., (886) 692-1076, hair clip, COD
2, Cecil, Toledo, OH 43612, (791) 560-1299, toy soldier, PAYPAL
3, Clarence, Port Saint Lucie, (791) 560-1299, book of jokes, CREDIT CARD
4, Clive, Warwick, RI 02886, (749) 409-1970, sharpie, CREDIT CARD
5, Maureen Massillon, OH 44646, (500) 539-2735, shoes, DEBIT CARD
```

可以使用以下代码检索列名。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// This is the source of the csv file
// It can be a link or the location of the File
const source = 'SampleData.csv'

async function run() {

   // Creating Dataset from the source
   const csvDataset = tf.data.csv(Source);

   // Retrieving the column names from the
   // dataset using columnNames function
   const ColumnNames = (await csvDataset.columnNames());

   // Printing the ColumnNames
   console.log(ColumnNames)
}

await run();
```

**输出:**

```
S No., UserName, Address, Mobile number, Item Ordered, Payment Type
```

**例 2:** 考虑以下 CSV 文件

```
S No, Name, Marks(out of 100)
1, Geek 1, 31
2, Geek 2, 65
3, Geek 3, 97
4, Geek 4, 75
5, Geek 5, 58
```

可以使用以下代码检索列名。

## Javascript

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// This is the source of the csv file
// It can be a link or the location of the File
const source = 'sample.csv'

async function run() {

   // Creating Dataset from the source
   const csvDataset = tf.data.csv(Source);

   // Retrieving the column names from
   // the dataset using columnNames function
   const ColumnNames = (await csvDataset.columnNames());

   // Printing the ColumnNames
   console.log(ColumnNames)
}

await run();
```

**输出:**

```
S No,Name,Marks(out of 100)
```

**参考:**T2】https://js.tensorflow.org/api/latest/#class:data.CSVDataset