# p5.js | p5。表 getColumn()方法

> 原文:[https://www . geesforgeks . org/P5-js-P5-table-getcolumn-method/](https://www.geeksforgeeks.org/p5-js-p5-table-getcolumn-method/)

p5 的 **getColumn()方法**。p5.js 中的表用于检索给定列中的所有值，并以数组的形式返回它们。要返回的列可以以其标题或标识的形式给出。
**语法:**

```
getColumn( column )

```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **列:**是一个字符串或数字，表示要返回的列的标题或编号。

**返回值:**返回列参数指定的列值数组。
以下示例说明了 p5.js 中的 **getColumn()函数【T4:
**示例:**** 

## java 描述语言

```
function setup() {
  createCanvas(500, 200);
  textSize(16);

  getColBtn = createButton("Get Column Values");
  getColBtn.position(30, 50);
  getColBtn.mouseClicked(getCols);

  text("Click on the button to get column values", 20, 20);

  // Create the table
  table = new p5.Table();

  // Add two columns
  // using addColumn
  table.addColumn("author");
  table.addColumn("language");

  // Add two rows
  let newRow = table.addRow();
  newRow.setString("author", "Dennis Ritchie");
  newRow.setString("language", "C");

  newRow = table.addRow();
  newRow.setString("author", "Bjarne Stroustrup");
  newRow.setString("language", "C++");
}

function getCols() {

  // Array of values in the column "author"
  author_col = table.getColumn("author");

  text("Column author: ", 20, 100);
  // Loop through the array to display the values
  for (let i = 0; i < author_col.length; i++) {
    text(author_col[i], 170 + i * 120, 100);
  }

  // Array of values in the column "language"
  language_col = table.getColumn("language");

  text("Column language: ", 20, 120);
  // Loop through the array to display the values
  for (let i = 0; i < language_col.length; i++) {
    text(language_col[i], 170 + i * 120, 120);
  }
}
```