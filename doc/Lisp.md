`sudo apt-get install libedit-dev  `


### 交互 `REPL`

- `read-evaluate-print loop` （读取 - 求值 - 输出循环）这种模式下的程序读取用户的输入，在程序内部进行处理，然后返回一些信息给用户。这种系统也被叫做 REPL

### 语法解析器

用来判断用户的输入是否合法，并产生解析后的内部表示。内部表示是一种计算机更容易理解的表示形式，有了它，我们后面的解析、求值等工作会变得更加的简单可行。

### `mpc` 库

解析器组合子 (Parser Combinators) 库、以使用这个库为任何语言编写语法解析器

`mpc`用法熟悉

### 柴犬语（Doge）

`Doge` 语言的语法描述：

- 形容词 (`Adjective`) 包括 `wow`、`many`、`so`、`such` 符号。
- 名词 (`Noun`) 包括 `lisp`、`language`、`c`、`book`、`build` 符号。
- 短语 (`Phrase`) 由形容词 (`Adjective`) 后接名词 (`Noun`) 组成。
- `Doge` 语言由 0 到多个 短语 (`Phrase`) 组成。

## 树型结构

内部结构就是上一章中打印出来的内容。它被称为*抽象语法树*(Abstract Syntax Tree，简称 AST)。它用来表示用户输入的表达式的结构。操作数和操作符等需要被处理的实际数据都位于叶子节点上。而非叶子节点上则包含了遍历和求值的信息。
