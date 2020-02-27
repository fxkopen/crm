# Fx.location

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fx.location：和查询归属地有关的API  

####1、查询单个号码归属地-findByMobile

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义：Fx.location.findByMobile(&lt;String mobile&gt;)

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     def(error,data,errorMessage) = Fx.location.findByMobile("13000000000")


----------


####2、批量查询手机号归属地-findByMobiles

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义：Fx.location.findByMobiles( [ List&lt;String&gt; mobiles ] )

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>     def(error,data,errorMessage) = Fx.location.findByMobiles(["13011111111","13000000000"])

