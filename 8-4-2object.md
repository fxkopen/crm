# Fx.object


Fx.object：和对象操作有关的API    

####1、创建业务对象-create
 - **普通新建**：Fx.object.create(&lt;String apiName&gt;,&lt;Map objectData&gt;)

&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

 参数 |说明|
-|-
apiName | 对象的api名称
objectData | 对象数据即字段值

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp; 举例：

 >     def(Boolean error,Map data,String errorMessage) = Fx.object.create("AccountObj",["name":"客户"])



----------


  - **对象创建同时新建从对象**：Fx.object.create(&lt;String apiName&gt;,&lt;Map&lt;String,Map&gt; objectData&gt;,&lt;Map details&gt;,&lt;boolean withBizLogic&gt;)

&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
-|-
apiName | 对象的api名称
objectData | 主对象数据即字段值
details | 从对象数据
withBizLogic | 和上面普通新建的标识性属性，默认为true

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp; 举例：

 >      def(Boolean error,Map data,String errorMessage) = Fx.object.create("object_2fJ1o__c",["name":"主从同时新建 主1"],["object_Ssm46__c":[["name":"张三1"]]],true)

&nbsp;&nbsp;&nbsp;&nbsp;注：对象创建同时新建从对象走新建对象业务逻辑（判断权限、触发审批流工作流等）

----------

####2、批量新建-batchCreate
 - **普通新建**：Fx.object.batchCreate(&lt;String apiName&gt;,&lt;List&lt;Map&gt; objectData&gt;)

&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
-|-
apiName | 对象的api名称
objectData | 对象数据即字段值

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp; 举例：

 >      def(Boolean error,List data,String errorMessage) = Fx.object.batchCreate("AccountObj",[["name":"客户1"],["name":"客户2"]])

&nbsp;&nbsp;&nbsp;&nbsp; 注：batch类函数不会触发审批流

----------

####3、更新业务对象-update
 - **定义**：Fx.object.update(&lt;String apiName&gt;,&lt;String objectDataId&gt;,&lt;Map objectData&gt;)

 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectDataId | 对象实例的ID
objectData | 对象数据即字段值

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) =  Fx.object.update("AccountObj","id123456",["name":"纷享销客"])

----------
####4、批量更新业务对象-batchUpdate
 - **定义**：Fx.object.batchUpdate(&lt;String apiName&gt;,&lt;Map&lt;String,Map&gt; objectData&gt;)

 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectData | 对象数据即字段值（key值为对象ID）

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：List

 - **举例：**


 >     def (Boolean error,List data,String errorMessage) =  object.batchUpdate("AccountObj",["e6a338ae8a944cdfb2bae737db1aa12f":["name":"客户1"],"4cd5a9f902af4f66a34df35a53630237":["name":"客户2"]])

&nbsp;&nbsp;&nbsp;&nbsp; 注：batch类函数不会触发审批流

----------


####5、按业务对象Id查询业务对象数据象-findById
 - **定义**：Fx.object.findById(&lt;String apiName&gt;,&lt;String objectDataId&gt;)
 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectDataId | 对象实例的ID

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) =  Fx.object.findById("AccountObj","e6a338ae8a944cdfb2bae737db1aa12f") 

----------

####6、批量按业务对象Id查询业务对象数据-findByIds
 - **定义**：Fx.object.findByIds(&lt;String apiName&gt;,&lt;List objectDataIds&gt;)
 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectDataIds | 对象实例的ID的List

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：List

 - **举例：**


 >     def (Boolean error,List data,String errorMessage) =  Fx.object.findByIds("AccountObj",["e6a338ae8a944cdfb2bae737db1aa12f","4cd5a9f902af4f66a34df35a53630237"]) 

----------


####7、按查询条件查询业务对象-find
 - **普通查询**：Fx.object.find(&lt;String apiName&gt;,&lt;List&lt;Map&gt; criteria&gt;,&lt;BigDecimal limit&gt;,&lt;BigDecimal skip&gt;)
参数说明：

参数 |说明|
 -|-
apiName | 对象的api名称
criteria | 查询条件
limit | 限制查询条数，最大200条，如超过返回200条
skip | 分页页数

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：QueryResult

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >     def (Boolean error,QueryResult data,String errorMessage) =  Fx.object.find("AccountObj",[["name":"纷享销客"],["create_time": Operator.GT(19000000)]],10,1); 

 - **查询并排序**：Fx.object.find(&lt;String apiName&gt;,&lt;List&lt;Map&gt; criteria&gt;,&lt;Map orderBy&gt;,&lt;BigDecimal limit&gt;,&lt;BigDecimal skip&gt;)
参数说明：

参数 |说明|
 -|-
apiName | 对象的api名称
criteria | 查询条件
limit | 限制查询条数，最大200条，如超过返回200条
orderBy | 排序规则  key:按哪个字段排序，字段名称 ；value：1 - 升序，-1 - 降序
skip | 分页页数

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：QueryResult

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >     def (Boolean error,QueryResult data,String errorMessage) =  Fx.object.find("AccountObj",[["name":"分享逍客"],["create_time": Operator.GT(19000000)]],["name":1],10,1);

Fx.object.find方法中的条件语句（使用Operator.调用，如 Operator.GT(19000000)）如下：

说明 |代码格式
 -|-
判断相等 | EQ(&lt;Object str&gt;)
判断不相等 | NE(&lt;Object str&gt;)
判断大于 | GT(&lt;Object str&gt;)
判断小于 | LT(&lt;Object str&gt;)
判断大于等于 | GTE(&lt;Object str&gt;)
判断小于等于 | LTE(&lt;Object str&gt;)
判断是否包含 | LIKE(&lt;String str&gt;)
判断不包含 | NLIKE(&lt;String str&gt;)
判断属于其中一个 | IN(&lt;List str&gt;)
判断不属于其中 | NIN(&lt;List list&gt;)
判断字段是否有值 | EXISTS(&lt;boolean ex&gt;)

----------

####8、作废业务对象-remove
 - **定义**：Fx.object.remove(&lt;String apiName&gt;,&lt;String objectDataId&gt;)
 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectDataId | 对象实例的ID

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) =  Fx.object.remove("AccountObj","ed47841898054749a2ec9be9e6e5d728")

----------
####9、更换负责人-changeOwner
 - **定义**：Fx.object.changeOwner(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;String OwnerId&gt;)
 - **参数说明**：

参数 |说明|
 -|-
apiName | 对象的api名称
objectDataId | 对象实例的ID
OwnerId | 要变更的负责人的用户ID

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map


 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.changeOwner("AccountObj","ed47841898054749a2ec9be9e6e5d728","1001")

----------
####10、添加团队成员-addTeamMember
 - **定义**：Fx.object.addTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List UserIdList&gt;,&lt;Integer Role&gt;,&lt;Integer Permission&gt;)
 - **参数说明**：

参数 |说明|
 -|-
ObjectAPIName | 对象的api名称
ObjectDataId | 对象实例的ID
UserIdList | 添加的团队成员的用户ID的List
Role | 添加的团队成员的角色：1-负责人，2-联合跟进人，3-售后服务人员，4-普通成员
Permission | 添加的团队成员的权限：1-只读，2-读写

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.addTeamMember("AccountObj","83cf73d957924284a96e9c44ebb333ec",["1001"],4,1)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：不能添加负责人；如果添加的成员包括负责人，则不会修改负责人数据；如果添加的成员在原系统中有重复的则更新该成员

----------
####11、删除团队成员-deleteTeamMember
 - **定义**：Fx.object.deleteTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List UserIdList&gt;)
 - **参数说明**：

参数 |说明|
 -|-
ObjectAPIName | 对象的api名称
ObjectDataId | 对象实例的ID
UserIdList | 删除的团队成员的用户ID的List

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.deleteTeamMember("AccountObj","83cf73d957924284a96e9c44ebb333ec",["1001"]) 

----------
####12、编辑团队成员-editTeamMember
 - **定义**：Fx.object.editTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List&lt;Map&gt; TeamMemberList&gt;)

 - **参数说明**：

参数 |说明|
 -|-
ObjectAPIName | 对象的api名称
ObjectDataId | 对象实例的ID
TeamMemberList | 要编辑团队成员的信息的List（key值包括：userID：用户ID；role：用户角色；permisson：用户权限，具体参考7）

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.editTeamMember("AccountObj","36fd270a986842529445bf3d252cca9b",[["userId":"1058","role":4,"permission":1],["userId":"1057","role":3,"permission":2]]) 

----------
####13、获取团队成员-getTeamMember
 - **定义**：Fx.object.getTeamMember(&lt;String objectAPIName&gt;,&lt;String objectId&gt;)
 - **参数说明**：

参数 |说明|
 -|-
objectAPIName | 对象的api名称
objectId | 对象实例的ID

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.getTeamMember("AccountObj","83cf73d957924284a96e9c44ebb333ec")

----------
####14、添加外部团队成员-addOutTeamMember
 - **定义**：Fx.object.addOutTeamMember(String apiName,String objectId,int permission,List&lt;Map&gt; employee) 

- **参数说明**：

参数 |说明|
 -|-
apiName | 对象的apiname
objectId | 对象实例的ID
permission | 外部团队成员权限 1：只读  2：读写
employee | 员工信息，其中Map包括【 userId：员工Id ； outTenantId：外部企业id】

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：String

 - **举例：**


 >     def (Boolean error,String data,String errorMessage) = Fx.object.addOutTeamMember('AccountObj',id,1,[['userId':'1001','outTenantId':'590057']])

----------
####15、获取单选/多选业务名称/选项名称-getOptionName
 - **定义**：Fx.object.getOptionName(&lt;String objectAPIName&gt;,&lt;String filedAPIName&gt;,&lt;String value&gt;)
 - **参数说明**：

参数 |说明|
 -|-
objectAPIName | 对象的api名称
filedAPIName | 字段的api名称
value | 单选/多选的值

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

 - **举例：**


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.getOptionName("AccountObj","lock_status","0")

----------
####16、根据映射规则创建数据-copyByRule
 - **根据映射规则新建（不能添加额外的字段）**：Fx.object.copyByRule(&lt;String sourceApiName&gt;,&lt;String sourceId&gt;,&lt;String ruleApiName&gt;)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
 -|-
sourceApiName | 被映射的对象Api Name
sourceId | 被映射的对象实例的ID
ruleApiName | 映射规则API Name

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：


 >     def (Boolean error,Map data,String errorMessage) = Fx.object.copyByRule('object_ejyW2__c','5d308dc0b5a2bf0001b0bfc2','map_btp50__c')

- **根据映射规则直新建（同时新建从对象）**：Fx.object.copyByRule(&lt;String sourceApiName&gt;,&lt;String sourceId&gt;,&lt;String ruleApiName&gt;,&lt;Map plus&gt;,  &lt;Map detailPlus&gt;)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
 -|-
sourceApiName | 被映射的对象Api Name
sourceId | 被映射的对象实例的ID
ruleApiName | 映射规则API Name
plus | 主对象数据参数
detailPlus | 从对象数据参数

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：Map

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：

 >     Map plus = ["field_ZszsO__c": "18800154471"];
 >     Map detailValues1 = ["field_z5AI0__c": "data1填充内容"]; 
 >     Map detailValues2 = ["field_z5AI0__c": "data2填充内容"];
 >     List  detailFillValueList= [];
 >     detailFillValueList.add( detailValues1);
 >     detailFillValueList.add( detailValues2);
 >     Map detailPlus = ["object_6hN1i__c": detailFillValueList]
 >     def (Boolean error,Map data,String errorMessage) = Fx.object.copyByRule('object_ob2G0__c','5cedf0137cfed9b33b75ddaa','map_797K4__c',plus,detailPlus)

----------
####17、数据锁定/解锁-lock/unlock
 - **数据锁定**：Fx.object.lock(String apiName , String objectId , boolean cascadeDetail)
 - **数据解锁**：Fx.object.unlock(String apiName , String objectId , boolean cascadeDetail)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
 -|-
apiName | 对象的apiname
objectId | 对象实例id
cascadeDetail | 是否锁定/解锁从对象

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：


 >     def (Boolean error,data,String errorMessage) =Fx.object.lock('AccountObj' , 'e6a338ae8a944cdfb2bae737db1aa12f' , true)

----------
####18、聚合计算-aggregate
 - **定义**：Fx.object.aggregate(String apiName,Aggregate type,int decimalScale,List criteria)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;参数说明：

参数 |说明|
 -|-
apiName | 对象的apiname
Aggregate | 计算类型
decimalScale | 小数位数
criteria | 查询条件（和find查询条件使用一样）

其中计算类型：

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Aggregate.SUM(String fieldApiName)**   求和  
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Aggregate.COUNT()**                    计算数量

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Aggregate.MAX(String fieldApiName)**   最大值

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Aggregate.MIN(String fieldApiName)**   最小值

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Aggregate.AVG(String fieldApiName)**   平均值

&nbsp;&nbsp;&nbsp;&nbsp; data返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;举例：


 >     def (Boolean error,String data,String errorMessage) =Fx.object.aggregate("object_rqa45__c",Aggregate.AVG("field_VE1by__c"),2,[["name":Operator.LIKE("name")])


