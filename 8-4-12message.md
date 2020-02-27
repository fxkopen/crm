# Fx.message

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fx.location：和发送消息有关的API  

#####Channel决定消息发送的类型

>     Channel channel = Channel.Service("appiD") //发送服务号

>     Channel channel = Channel.ObjectSession("ObjectAPIName","ObjectId") //发送业务群

 - **参数说明**：

参数 |说明|
-|-
appId | 服务号的appId
ObjectAPIName | 业务群所属对象API Name
ObjectId | 业务群所属对象实例Id

####1、发送文本消息

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义：Fx.message.send(String textMessage , List&lt;Integer&gt; receiverIds , &lt;Channel channel&gt;)

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：通过appId为FSAID_bebd374的服务号向ID为1000的用户发送一条文本消息-”这是一条文本消息“

>     Channel channel = Channel.Service("FSAID_bebd374")

>     List receiverIds = [1000] //消息接收用户

>     def (error,date,errorMessage) = Fx.message.send("这是一条文本消息",receiverIds,channel)

----------


####2、发送卡片消息

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;定义：Fx.message.send(&lt;Card card&gt; ,  &lt;List&lt;Integer&gt;receiverIds&gt; , &lt;Channel channel&gt;)

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例1：向ID为5cbd28e47cfed9ea0cca09e4的客户群发送一个点击跳转对象详情页的卡片消息

>     def card = ObjectCard.builder {
>       head {
>         title = "head title" //卡片标题(必填)
>       }
>       foot {
>         title = "foot title" //卡片底部(必填)
>       }
>       body {
>         content = "body content" //卡片内容(必填)
>         entries = [key: "value"] //卡片表格(可选)
>       }
>       objectApiName = "AccountObj" //跳转对象的APIName(必填)
>       objectId = "5cbd28e47cfed9ea0cca09e4" //跳转对象的id(必填)
>     }
>     Channel channel = Channel.ObjectSession("AccountObj","5cbd28e47cfed9ea0cca09e4")
>     List receiverIds = [1000]
>     def (error,date,errorMessage) = Fx.message.send(card,receiverIds,channel)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例2：通用卡片，跳转至其他地址

>     def card = Card.builder {
>       head {
>         title = "head title"
>       }
>       foot {
>         title = "foot title"
>       }
>       body {
>         content = "body content"
>         entries = [key: "value"]
>       }
>       innerDirectWebUrl = "web" //卡片消息连接地址，纷享内部平台Web端跳转(可选)
>       innerDirectMobileUrl = "mobile" //卡片消息连接地址，纷享内部平台手机端端跳转(可选)
>       outerDirectUrl = "outer"  //卡片消息连接地址，外部平台跳转(可选)
>     }
>     Channel channel = Channel.Channel.Service("FSAID_bebd374")
>     List receiverIds = [1000]
>     def (error,date,errorMessage) = Fx.message.send(card,receiverIds,channel)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**注：**1、向业务群发送消息时，是通过客户助手发送到群对话中，群成员全部可见，receiverIds定义无效，但是参数必须存在

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2、向服务号发送消息时，如果receiverIds不在该服务号的可见范围内，则不会发送成功
