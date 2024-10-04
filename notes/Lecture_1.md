# 第1课
[英文原版](https://cs50.harvard.edu/python/2022/notes/1/)
## 条件语句

- 条件语句允许作为程序员的您，让程序做出决策：就好像您的程序可以根据某些条件选择走左边的路还是右边的路。
- Python内置了一套用于提出数学问题的“运算符”。
- `>` 和 `<` 符号您可能已经很熟悉了。
- `>=` 表示“大于或等于。”
- `<=` 表示“小于或等于。”
- `==` 表示“等于，但请注意双等号！单个等号会赋值。双等号用于比较变量。
- `!=` 表示“不等于。”
- 条件语句将左边的项与右边的项进行比较。


## if语句

- 在您的终端窗口中，输入`code compare.py`。这将创建一个名为“compare”的新文件。
- 在文本编辑器窗口中，从以下内容开始：
```
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
```
- 请注意，您的程序如何接收用户对x和y的输入，将它们转换为整数，并将它们保存到各自的x和y变量中。然后，if语句比较x和y。如果满足x < y的条件，将执行打印语句。
if语句使用布尔值（true 或 false）来决定是否执行。如果x > y的语句为真，编译器将将其注册为真并执行代码。

## 控制流、elif 和 else
进一步修改你的代码如下：

```
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
if x > y:
    print("x is greater than y")
if x == y:
    print("x is equal to y")
```

注意你正在提供一系列语句。首先，第一个语句被评估。然后，第二个语句（如果第一个语句为假）会进行评估（但在这里我们使用 `elif` 来避免不必要的评估，如果第一个条件为真，则不会检查第二个条件）。最后，如果前面的条件都不满足，则执行最后一个 `else` 语句。这种决策流程被称为“控制流”。

我们的代码可以表示如下：
<img src="https://github.com/user-attachments/assets/bcbd35f8-27de-45fe-b6fa-cd37f9b1bd7c" width="200" />

