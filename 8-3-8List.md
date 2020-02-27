# List类型

List - 集合类型，使用时用[]封装，中间数据用,分隔

定义List：`List list = []`

例：

>     List colors = ["red","blue","green","yellow"]

List类型的方法：

 - **list.add(&lt;Object any_type&gt;)**：向列表添加元素
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green"]

>     colors.add("yellow") //返回：true


----------


 - **list.addAll(&lt;List list1&gt;)**：向列表添加多个元素
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue"]

>     colors.addAll(["green", "yellow"]) //返回：true


----------


 - **list.clear()**：清空字符串
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：无返回值

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue"]

>     colors.clear()


----------


 - **list.contains(&lt;Object any_type&gt;)**：判断列表中是否存在指定元素。如果列表中存在元素, 则返回"true"
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green", "yellow"]

>     result = colors.contains("red") //返回：true


----------


 - **list.containsAll(&lt;List list1&gt;)**：判断列表中是否存在所有指定元素。如果列表中存在元素, 则返回"true"
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green"]

>     result = colors.containsAll(["red", "yellow"]) //返回：false


----------


 - **list.indexOf(&lt;Object any_type&gt;)**：返回给定元素在列表中的位置 (第一个元素的位置为 "0")
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      List colors = ["red", "blue", "green", "yellow"]

>      result = colors.indexOf("green") //返回：2


----------


 - **list.get(&lt;BigDecimal indexNumber&gt;)**：返回给定位置在列表中的元素 (第一个元素的位置为 "0")
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Object

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      List colors = ["red", "blue", "green", "yellow"]

>      result = colors.get(1) // 返回: "blue"


----------


 - **list.size()**：返回列表中元素的数目
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green", "yellow"]

>     result = colors.size() //返回：4


----------


 - **list.sort(&lt;Boolean bool&gt;)**列表排序,可选布尔值指定升序 (true)/降序 (false),为空时默认为升序
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green", "yellow"]

>     colors.sort() // 返回: ["blue","green","red","yellow"]


----------


 - **list.subList(&lt;BigDecimal startIndex&gt;,&lt;BigDecimal endIndex&gt;)** 根据指定的开始和结束索引 (包含指定的索引) 从给定列表中返回一组元素
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     List colors = ["red", "blue", "green", "yellow"]

>     result = colors.sublist(1, 3); // 返回: ["blue","green","yellow"]


----------


 - **list.remove(&lt;BigDecimal index&gt;)**移除并返回指定索引处的元素 (第一个元素的索引为 "0")
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Object

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      List colors = ["red", "blue", "green", "yellow"]

>      colors.remove(2) // 返回: "green"


----------


 - **list.isEmpty()**判断列表是否为空。返回一个布尔值-如果列表中不包含任何值, 则为true; 否则为-如果列表中包含值, 则为false
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      List colors = ["red", "blue", "green", "yellow"]

>      result = colors.isEmpty() // 返回: false


----------


 - **list.intersect(&lt;List list&gt;)** 返回指定列表与当前列表的交集
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      colors = ["red", "blue", "green", "orange"]
> 
>      fruits = ["apple","orange","banana"]
> 
>      result = colors.intersect(fruits) // 返回：["orange"]


----------


 - **list.lastIndexOf(&lt;Object any_type&gt;)** 返回指定元素在列表中的最后一个匹配项的位置
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       colors = ["red", "blue", "green", "yellow", "green"]
> 
>       result = colors.lastIndexOf("green") //返回：4


----------


 - **list.eachWithIndex(&lt;Closure closure&gt;)** 遍历列表中的数据，闭包中传入item和index
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       List list = ["a", "c"]
> 
>       list.eachWithIndex { item, int i ->
> 
>           log.info(item)

>           log.info(i)
> 
>       } //运行日志：a  0  b  1


----------


 - **list.each(&lt;Closure closure&gt;)** 遍历列表中的数据，闭包中传入item
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       List list = ["a", "c"]
> 
>       list.each { item -> 
> 
>           log.info(item)

>       } //运行日志：a   b



----------


 - **list.any{&lt;Closure closure&gt;}** 判断是否至少有一个元素有效
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例1：

>       List list = ["a", "b"]
> 
>       Boolean b = list.any{x ->x=="a"} //list中是否有一个元素为"a"
> 
>       log.info(b)

>       } //运行日志：true

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例2：

>       List list = [["a":1], ["a":2]]
> 
>       Boolean b = list.any{x ->(x.a as Integer)>1} //list中元素为map，并且key为"a"的value值是否有一个大于1
> 
>       log.info(b)

>       } //运行日志：true

----------


 - **list.collect{&lt;Closure closure&gt;}** list中的元素为map，取出每个map中的value值
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       List list = [["a":1], ["a":2]]
> 
>       List list = list.collect{x ->x.a} 
> 
>       log.info(list)

>       } //运行日志：[1,2]

----------


 - **list.find{&lt;Closure closure&gt;}** list中的元素为map，取出每个map中第一个符合条件的value值
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       List list = [["a":1], ["a":2]]
> 
>       Map map = list.find{x ->(x.a as Integer)>1} 
> 
>       log.info(map)

>       } //运行日志：{a=2}


