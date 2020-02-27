# DateTime类型

Date - 日期类型（具体），格式为YYYY-MM-DD hh:mm，使用时用""封装

定义Date：`DateTime dateTime = "<YYYY-MM-DD hh:mm>"`

例：

>     DateTime dateTime = "2019-01-01 12:00"

DateTime类型的方法：

 - **DateTime.now()**：获取当前时间的年月日时分
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     DateTime d = DateTime.now()


----------


 - **dateTime.withYear(&lt;Integer year&gt;)**：设置日期的年，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：DateTime
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.withYear(2018) //返回：2018-01-01 12:00


----------


 - **dateTime.withMonth(&lt;Integer month&gt;)**：设置日期的月，返回新的日期
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：DateTime

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.withMonth(12) //返回：2019-12-01 12:00


----------


 - **dateTime.withDay(&lt;Integer day&gt;)**：设置日期的日，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：DateTime
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.withDay(30) //返回：2019-01-30 12:00


----------


 - **dateTime.withHour(&lt;Integer hour&gt;)**：设置日期的小时，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：DateTime
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.withHoue(13) //返回：2019-01-01 13:00


----------


 - **dateTime.withMinute(&lt;Integer day&gt;)**：设置日期的分钟，返回新的日期

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：DateTime
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.withMinute(30) //返回：2019-01-01 12:30


----------


 - **dateTime.toTimestamp()**：日期转时间戳

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     dateTime.toTimestamp() //返回：1568001600000


----------


 - **dateTime.year**：获取日期中的年

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      dateTime.year //返回：2019


----------


 - **dateTime.month**：获取日期中的月

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      dateTime.month //返回：1


----------


 - **dateTime.day**：获取日期中的日

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       dateTime.day //返回：1


----------


 - **dateTime.hour**：获取日期中的小时

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       dateTime.hour //返回：12


----------


 - **dateTime.minute**：获取日期中的分钟

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       dateTime.minute //返回：0




