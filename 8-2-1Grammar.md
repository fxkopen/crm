# 基本语法

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;自定义函数基本语法和通用计算机语言语法一致，如：

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <数据类型> <变量> = <表达式>

语法构成  |说明|
-|-
数据类型 | 在自定义函数中提供12大数据类型，具体可参考数据类型章节（区分大小写）
变量    | 即该数据的名称，用于在之后逻辑中的调用，可自定义设置（不可和数据类型一样）
表达式 | 即该变量被赋予的值，可以是被直接定义的也可为一个表达式（如果是表达式请注意表达式返回值类型要与数据类型一致，否则报错）

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**注：**在自定义函数中可用 def 表示数据类型，编译时自动识别数据类型
 
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**举例：**
 

>       String str = "fxiaoke" //被直接定义 

>       Boolean boo = ["red", "blue", "green", "yellow"].isEmpty() //表达式定义

>       def result = ["red", "blue", "green", "yellow"].isEmpty() //def表示数据类型
