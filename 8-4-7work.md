# Fx.work


Fx.work：和协同工作相关的API

####1、发任务-createTask

 - **定义**：Fx.work.createTask(&lt;String title&gt;,&lt;String content&gt;,&lt;DateTime deadLine&gt;,&lt;Map&lt;List&gt; executeUsers&gt;, &lt;Map&lt;List&gt; atUsers&gt;)

 - **参数说明**：

参数 |说明|
-|-
title | 任务标题
content | 任务内容
deadLine | 任务完成时间
executeUsers | 执行人
atUsers | 抄送范围


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：**executeUsers** map keys : "users" 用户 ，"departments" 部门

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**atUsers** map keys : "users" 用户 ，"departments" 部门

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >      DateTime deadLine = DateTime.now + 1.days
 
 >      Fx.work.createTask("hello", "world", deadLine, [users: ["1059"]], [users: ["1059","1025"],departments:["253937"]])

----------

####2、发日程-createSchedule

 - **定义**：Fx.work.createSchedule(&lt;String content&gt;,&lt;DateTime beginTime&gt;,&lt;DateTime endTime&gt;, &lt;boolean isFullDate&gt;,&lt;boolean needReceipt&gt;,&lt;List remindTimes&gt;,&lt;Map&lt;List&gt; atUsers&gt;)

 - **参数说明**：

参数 |说明|
-|-
content | 日程内容
beginTime | 日程开始时间
endTime | 日程结束时间
isFullDate | 是否全天日程
needReceipt | 是否需要回执
remindTimes | 提醒时间
atUsers | 抄送范围/参与人


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：**remindTimes枚举值**：

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1、RemindTime.BEGIN - 开始时；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2、RemindTime.FIVE_MINUTES_AGO：5分钟前；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3、RemindTime.FIFTEEN_MINUTES_AGO：15分钟前；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4、RemindTime.THIRTY_MINUTES_AGO-30分钟前；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5、RemindTime.ONE_HOURS_AGO-1小时前；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6、RemindTime.TWO_HOURS_AGO -2小时前

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**atUsers** map keys : "users" 用户 ，"departments" 部门

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >      DateTime endTime = DateTime.now + 1.hours
 
 >      Fx.work.createSchedule("hello", DateTime.now(), endTime , false, false, [RemindTime.BEGIN()], [users: ["1000","1002"]])

----------
####3、发销售记录-createSalesRecord

 - **定义**：Fx.work.createSalesRecord(&lt;String content&gt;,&lt;Map objects&gt;,&lt;Map&lt;List&gt; atUsers&gt;)

 - **参数说明**：

参数 |说明|
-|-
content | 销售记录内容
objects | 关联对象
atUsers | 抄送范围

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：**objects** map keys ："object_api_name" 对象APIName ,  "id" 对象Id

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**atUsers** map keys : "users" 用户 ，"departments" 部门

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >     Fx.work.createSalesRecord("hello",[[object_api_name:"AccountObj",id:"4d79c3068aca42b28aebbc98223e8bed"]], [users:["1025"]])


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：不支持选销售记录类型






