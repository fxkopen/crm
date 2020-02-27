# Fx.http

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fx.http：和http请求相关的API  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;其中content属性类型为String/Map，根据HTTP返回头Content-Type中是否包含application/json来决定content类型，True是Map，False是String；

####1、HTTP GET请求息-get

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**定义1**：Fx.http.get(String url,Map headers)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data返回值类型：HttpResult，属性有：statusCode、content

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：
>     def (Boolean error,HttpResult data,String errorMessage) =  Fx.http.get("http://www.fxiaoke.com",["X-token":"myToken"])

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**定义2**：Fx.http.get(String url , Map headers , int timeout , boolean retry, int retryCount)

&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

 参数 |说明|
-|-
url | 请求地址
headers | 请求header
timeout | scoketTimeOut超时时间，单位ms，最大10s ，1s=1000ms
retry | scoketTimeOut超时是否重试；连接超时一定会进行重试，这个参数决定了timeout是否重试；设置为true时，可能会造成重复提交
retryCount | 重试次数，最多3次

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data返回值类型：HttpResult，属性有：statusCode、content

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：
>     def (Boolean error,HttpResult data,String errorMessage) =  Fx.http.get("http://www.fxiaoke.com",["X-token":"myToken"],2000,true,2)

----------


####2、HTTP POST请求-post

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**定义1**：Fx.http.post(String url,Map headers,Map/String data)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data返回值类型：HttpResult，属性有：statusCode、content

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：
>     def (Boolean error,HttpResult data,String errorMessage) =  Fx.http.post("http://www.fxiaoke.com",["X-token":"myToken"],["id":1])

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**定义2**：Fx.http.post(String url , Map headers , Map/String data , int timeout , boolean retry, int retryCount)

参数 |说明|
-|-
url | 请求地址
headers | 请求header
data | 请求体
timeout | scoketTimeOut超时时间，单位ms，最大10s ，1s=1000ms
retry | scoketTimeOut超时是否重试；连接超时一定会进行重试，这个参数决定了timeout是否重试；设置为true时，可能会造成重复提交
retryCount | 重试次数，最多3次

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;data返回值类型：HttpResult，属性有：statusCode、content

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：
>     def (Boolean error,HttpResult data,String errorMessage) =  Fx.http.post("http://www.fxiaoke.com",["X-token":"myToken"],["id":1],2000,true,2)



