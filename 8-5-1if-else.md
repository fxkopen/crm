# if-else

&nbsp;&nbsp;&nbsp;用来判定所给定的条件是否满足，根据判定的结果（真或假）决定执行哪个操作

- **定义**：

>       if(条件1) {

>           如果条件1为真，则执行这里

>       }else if(条件2){

>           如果条件2为真，则执行这里

>       }else {

>           如果条件1和条件2都不为真，则执行这里

>       }

&nbsp;&nbsp;&nbsp;注：在if控制语句中必须存在if和else控制语句，else if可以有0个或多个，根据实际场景使用

- **举例**：

>       String str = "fxiaoke"

>       if(str.contains("s")) {

>           str = "hello"

>       }else if(str.contains("f")){

>           str = "welcome"

>       }else {

>           str = "hi"

>       }//最终结果 str=welcome
