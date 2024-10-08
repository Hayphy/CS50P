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

<img src="https://github.com/user-attachments/assets/bcbd35f8-27de-45fe-b6fa-cd37f9b1bd7c" width="300" />

此程序可以通过避免连续提出三个问题来进行改进。毕竟，这三个问题不可能同时得出“非”（即不可能同时不满足所有条件）。请按如下方式修改你的程序：

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x 小于 y")
elif x > y:
    print("x 大于 y")
elif x == y:
    print("x 等于 y")
```

注意，通过使用`elif`可以使程序做出的决策更少。首先，会评估第一个条件语句。如果此语句为真，则后面的所有语句都不会执行。然而，如果第一个条件语句评估为假，则会评估第二个`elif`条件。如果第二个条件为真，则不会执行最后的评估。

我们的代码可以表示如下：

虽然从速度上来说，你的计算机可能无法区分我们的第一个程序和修改后的程序之间的差异，但想象一下，如果在线服务器每天运行数十亿或数万亿次这种类型的计算，那么这样一个小的编码决策肯定会产生影响。

我们的程序还可以做最后一项改进。注意，从逻辑上讲，`elif x == y`这个评估是不必要的。毕竟，如果逻辑上x不小于y且x不大于y，那么x必定等于y。因此，我们不必运行这个评估。我们可以使用`else`语句来创建一个“包罗万象”的默认结果。我们可以按如下方式修改：

```python
x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x 小于 y")
elif x > y:
    print("x 大于 y")
else:
    print("x 等于 y")
```

注意，通过我们的修改，此程序的相对复杂性已经降低。

我们的代码可以表示如下：

