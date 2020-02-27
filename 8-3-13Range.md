# Range类型


&nbsp;&nbsp;&nbsp;在自定义函数中不支持for循环，但是可以用Range完成循环语句逻辑

- **定义**：

>       Range range = Ranges.of(Integer start,Integer end)

>       range.each{

>       }

&nbsp;&nbsp;&nbsp;**注**：最多循环200次


- **举例**：

>       Range range = Ranges.of(1,5)

>       range.each{
 
>           it ->
     
>       }  //返回：[1,2,3,4,5]

