# Date类型

Date - 日期类型，格式为YYYY-MM-DD，使用时用""封装

定义Date：`Date date = "<YYYY-MM-DD>"`

例：

>     Date date = "2019-01-01"

Date类型的方法：


----------


 - **Date.now()**：获取当前时间的年月日
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     Date d = Date.now()


----------


 - **date.withYear(&lt;Integer year&gt;)**：设置日期的年，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Date
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     date.withYear(2018) //返回：2018-01-01


----------


 - **date.withMonth(&lt;Integer month&gt;)**：设置日期的月，返回新的日期
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Date

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     date.withMonth(12) //返回：2019-12-01


----------


 - **date.withDay(&lt;Integer day&gt;)**：设置日期的日，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Date
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     date.withDay(30) //返回：2019-01-30


----------


 - **date.toTimestamp()**：日期转时间戳

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     date.toTimestamp() //返回：1567958400000


----------


 - **date.year**：获取日期中的年

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     date.year //返回：2019


----------


 - **date.month**：获取日期中的月

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      date.month //返回：1


----------


 - **date.day**：获取日期中的日

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      date.day //返回：1


