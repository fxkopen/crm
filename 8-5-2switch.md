# switch


&nbsp;&nbsp;&nbsp;用来判定所给定的条件是否满足，根据判定的结果（真或假）决定执行哪个操作

- **定义**：

>       switch(<key>){

>           case <value-1>: statements-1; break;

>           case <value-2>: statements-2; break;

>           default: statements-3; break;

>       }

>       //执行顺序：当key值和value-1的值一样时，执行statements-1并结束；如果key和value-1值不等，但等于value-2时，执行statements-2并结束；...;如果都不相等，则执行statements-3并结束

&nbsp;&nbsp;&nbsp;**注**：1、case语句可以存在多个；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2、可以没有default语句，但为防止因未在case语句中匹配到与key值相等的value报错，尽量存在一个（最多一个）default语句；

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3、在每个case和default语句后可以没有break;语句，表示不结束switch语句，继续执行，如在上例中没有break语句，假设key和value-2相等，则在执行完statements-2后会再执行statements-3

- **举例**：


>       Integer = 3

>       switch (day) {

>            case 0:   x="Today it's Sunday";    break;

>            case 1:   x="Today it's Monday";    break;

>            case 2:   x="Today it's Tuesday";   break;

>            case 3:   x="Today it's Wednesday"; break;

>            case 4:   x="Today it's Thursday";  break;

>            case 5:   x="Today it's Friday";    break;

>            case 6:   x="Today it's Saturday";  break;

>       }//最终结果 Today it's Wednesday




