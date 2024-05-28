# pandas
python pandas 使用指南
Pandas中的DataFrame数据类型API函数参考手册 一
目录
前言
一、构造函数(Constructor)
1. DataFrame
二、属性和基础数据(Attributes and underlying data)
1. DataFrame.index
2. DataFrame.columns
3. DataFrame.dtypes
4. DataFrame.info([verbose, buf, max_cols, ...])
5. DataFrame.select_dtypes([include, exclude])
6. DataFrame.values
7. DataFrame.axes
8. DataFrame.ndim
9. DataFrame.size
10. DataFrame.shape
11. DataFrame.memory_usage([index, deep])
12. DataFrame.empty
13. DataFrame.set_flags(*[, copy, ...])

目录
> # 前言
** Pandas 是一个专门用于数据处理和分析的 Python 库，它提供了众多强大的数据结构和函数，帮助用户更加轻松、高效地完成数据处理和分析任务。其中，DataFrame 数据类型是 Pandas 中非常重要的一种数据结构，可以方便地对二维表格数据进行操作、处理、统计和可视化等工作。**

Pandas 中 DataFrame 的一些特点和优势，比如：

可以灵活处理不同类型的数据，包括数字、文本、日期等等。
提供了许多强大的数据处理函数，比如过滤、排序、聚合等操作。
方便进行数据可视化和统计分析，例如可视化不同变量之间的关系、计算各种统计量等。
易于与其他 Python 库相集成使用，比如 NumPy、Matplotlib 等库。

# 一、构造函数(Constructor)
'''
 DataFrame([data, index, columns, dtype, copy])
''' 
#二维、大小可变、可能异构的表格数据。

## 1. DataFrame
### "class pandas.DataFrame(data=None, index=None, columns=None, dtype=None, copy=None)[source]"

pandas.DataFrame() 是用于创建 DataFrame 数据类型的类，其参数如下：

data：要传入 DataFrame 中的数据，可以是多种形式，包括 Numpy 数组、dicts、series、DataFrame 等。
index：DataFrame 的索引。行标签可以是数字或字符串。如果没有显示指定索引，则会默认生成整数 RangeIndex(0, 1, 2, …, n)索引。
columns：DataFrame 的列标签。必须提供列名。
dtype：指定 DataFrame 中元素的类型，可以是 Numpy 类型或 Python 内置类型，比如 float、int、str 等。只允许一个数据类型。
copy：如果复制输入数据，可以选择 True 或 False。
使用示例：

import pandas as pd

# 定义输入数据
data = {'name': ['Tom', 'Jerry', 'Mike', 'Jack'],
        'age': [24, 25, 22, 26],
        'city': ['Beijing', 'Shanghai', 'Guangzhou', 'Shenzhen']}

# 定义索引
index = ['a', 'b', 'c', 'd']

# 定义列标签
columns = ['name', 'age', 'city', 'salary']

# 定义元素类型
dtype = str

# 创建 DataFrame 对象
df = pd.DataFrame(data=data, index=index, columns=columns, dtype=dtype)

# 打印 DataFrame
print(df)
