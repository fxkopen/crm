# 函数清单

<table style="font-size:12px">
  <tr >
    <th>函数API</th>
    <th>函数方法</th>
    <th>描述</th>
    <th>data返回类型</th>
  </tr>
<tr>
    <td rowspan="5" >context</td>
  </tr>
<tr>
    <td >context.tenantId</td>
    <td>获取登录账号的企业ID</td>
    <td>String</td>

  </tr>
<tr>
    <td >context.userId</td>
    <td>获取登录账号的用户ID</td>
    <td>String</td>
  </tr>
<tr>
    <td >context.details</td>
    <td>获取绑定对象的明细数据</td>
    <td>Map</td>
  </tr>
<tr>
    <td >context.data</td>
    <td>获取绑定对象的全部数据（包含明细数据）</td>
    <td>Map</td>
  </tr>
  <tr>
    <td rowspan="23" >Fx.object</td>
  </tr>
  <tr>
    <td >Fx.object.create(&lt;String apiName&gt;,&lt;Map objectData&gt;)</td>
    <td>创建业务对象(普通新建)</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.create(&lt;String apiName&gt;,&lt;Map&lt;String,Map&gt; objectData&gt;,&lt;Map details&gt;,&lt;boolean withBizLogic&gt;)</td>
    <td>对象创建同时新建从对象</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.batchCreate(&lt;String apiName&gt;,&lt;List&lt;Map&gt; objectData&gt;)</td>
    <td>批量新建</td>
    <td>List</td>
  </tr>

  <tr>
    <td>Fx.object.update(&lt;String apiName&gt;,&lt;String objectDataId&gt;,&lt;Map objectData&gt;)</td>
    <td>更新业务对象</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.batchUpdate(&lt;String apiName&gt;,&lt;Map&lt;String,Map&gt; objectData&gt;)</td>
    <td>批量更新业务对象</td>
    <td>List</td>
  </tr>

  <tr>
    <td>Fx.object.findById(&lt;String apiName&gt;,&lt;String objectDataId&gt;)</td>
    <td>按业务对象Id查询业务对象数据象</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.findByIds(&lt;String apiName&gt;,&lt;List objectDataIds&gt;)</td>
    <td>批量按业务对象Id查询业务对象数据</td>
    <td>List</td>
  </tr>
  <tr>
    <td>Fx.object.find(&lt;String apiName&gt;,&lt;List&lt;Map&gt; criteria&gt;,&lt;BigDecimal limit&gt;,&lt;BigDecimal skip&gt;)</td>
    <td>按查询条件查询业务对象（普通查询）</td>
    <td>QueryResult</td>
  </tr>

  <tr>
    <td>Fx.object.find(&lt;String apiName&gt;,&lt;List&lt;Map&gt; criteria&gt;,&lt;Map orderBy&gt;,&lt;BigDecimal limit&gt;,&lt;BigDecimal skip&gt;)//orderBy的value值：1 - 升序，-1 - 降序</td>
    <td>按查询条件查询业务对象（查询并排序）</td>
    <td>QueryResult</td>
  </tr>

  <tr>
    <td>Fx.object.remove(&lt;String apiName&gt;,&lt;String objectDataId&gt;)</td>
    <td>作废业务对象</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.changeOwner(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;String OwnerId&gt;)</td>
    <td>更换负责人</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.addTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List UserIdList&gt;,&lt;Integer Role&gt;,&lt;Integer Permission&gt;)//Role:1-负责人，2-联合跟进人，3-售后服务人员，4-普通成员 ;Permission:1-只读，2-读写
</td>
    <td>添加团队成员</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.deleteTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List UserIdList&gt;)</td>
    <td>删除团队成员</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.editTeamMember(&lt;String ObjectAPIName&gt;,&lt;String ObjectDataId&gt;,&lt;List&lt;Map&gt; TeamMemberList&gt;)//TeamMemberList的key值包括：userID：用户ID；role：用户角色；permisson：用户权限</td>
    <td>编辑团队成员</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.getTeamMember(&lt;String objectAPIName&gt;,&lt;String objectId&gt;)</td>
    <td>获取团队成员</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.addOutTeamMember(String apiName,String objectId,int permission,List&lt;Map&gt; employee) </td>
    <td>添加外部团队成员</td>
    <td>String</td>
  </tr>

  <tr>
    <td>Fx.object.getOptionName(&lt;String objectAPIName&gt;,&lt;String filedAPIName&gt;,&lt;String value&gt;)</td>
    <td>获取单选/多选业务名称/选项名称</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.copyByRule(&lt;String sourceApiName&gt;,&lt;String sourceId&gt;,&lt;String ruleApiName&gt;)</td>
    <td>根据映射规则新建（无从对象）</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.copyByRule(&lt;String sourceApiName&gt;,&lt;String sourceId&gt;,&lt;String ruleApiName&gt;,&lt;Map plus&gt;,  &lt;Map detailPlus&gt;)</td>
    <td>根据映射规则直新建（同时新建从对象）</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.object.lock(String apiName , String objectId , boolean cascadeDetail)</td>
    <td>数据锁定</td>
    <td>null</td>
  </tr>

  <tr>
    <td>Fx.object.unlock(String apiName , String objectId , boolean cascadeDetail)</td>
    <td>数据解锁</td>
    <td>null</td>
  </tr>

  <tr>
    <td>Fx.object.aggregate(String apiName,Aggregate type,int decimalScale,List criteria)</td>
    <td>聚合计算</td>
    <td>String</td>
  </tr>

 <tr>
    <td rowspan="7" >Fx.org</td>
  </tr>

  <tr>
    <td>Fx.org.findUserById(&lt;String userId&gt;)</td>
    <td>按用户ID查询用户信息</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.org.findByUserIds(&lt;List userIdList&gt;)</td>
    <td>按用户Id列表查询若干用户信息</td>
    <td>Map</td>
  </tr>

  <tr>
    <td>Fx.org.findEmployeeByDepartmentId(String departmentId)</td>
    <td>根据部门id查员工信息</td>
    <td>List&lt;Map&gt;</td>
  </tr>

  <tr>
    <td>Fx.org.findDepartmentByIds(List&lt;String&gt; departmentIds)</td>
    <td>根据部门id查部门信息</td>
    <td>List&lt;Map&gt;</td>
  </tr>

  <tr>
    <td>Fx.org.findSuperordinateDepartments(String id，boolean recursion)</td>
    <td>根据部门id查上级部门信息</td>
    <td>Map&lt;String , Map&gt;</td>
  </tr>

  <tr>
    <td>Fx.org.findSubordinateDepartments(String id，boolean recursion)</td>
    <td>根据部门id查下级部门信息</td>
    <td>Map&lt;String , Map&gt;</td>
  </tr>

  <tr>
    <td rowspan="5" >Fx.http</td>
  </tr>

  <tr>
    <td>Fx.http.get(&lt;String url&gt;,&lt;Map headers&gt;)</td>
    <td>HTTP GET请求</td>
    <td>HttpResult </td>
  </tr>

  <tr>
    <td>Fx.http.get(String url , Map headers , int timeout , boolean retry, int retryCount)</td>
    <td>HTTP GET请求</td>
    <td>HttpResult </td>
  </tr>

  <tr>
    <td>Fx.http.post(&lt;String url&gt;,&lt;Map headers&gt;,&lt;Map/String data&gt;)</td>
    <td>HTTP POST请求</td>
    <td>HttpResult </td>
  </tr>

  <tr>
    <td>Fx.http.post(String url , Map headers , Map/String data , int timeout , boolean retry, int retryCount)</td>
    <td>HTTP POST请求</td>
    <td>HttpResult </td>
  </tr>

 <tr>
    <td rowspan="3" >Fx.log</td>
  </tr>

  <tr>
    <td>Fx.log.info(&lt;String string&gt;)或Fx.log.info(&lt;Object object&gt;)</td>
    <td>运行日志</td>
    <td>无</td>
  </tr>
  <tr>
    <td>Fx.log.debug(&lt;String string&gt;)  或 Fx.log.debug(&lt;Object object&gt;)</td>
    <td>调试日志</td>
    <td>无</td>
  </tr>

 <tr>
    <td rowspan="7" >Fx.crm</td>
  </tr>

  <tr>
    <td>Fx.crm.product.shelf(&lt;String 产品Id&gt;,&lt;Integer value&gt;) //value=1:上架;value=2:下架</td>
    <td>产品上架下架</td>
    <td>Map</td>  
  </tr>

  <tr>
    <td>Fx.crm.leads.giveBack(&lt;String 线索Id&gt;,&lt;String 线索池Id&gt;)</td>
    <td>线索退回</td>
    <td>Map</td>
  </tr>
  <tr>
    <td>Fx.crm.leads.move(&lt;String 线索Id&gt;,&lt;String 线索池Id&gt;)</td>
    <td>线索转移</td>
    <td>Map</td>
  </tr>
  <tr>
    <td>Fx.crm.account.move(&lt;String 客户Id&gt;, &lt;String 公海Id&gt;)</td>
    <td>客户转移公海</td>
    <td>Map</td>
  </tr>
  <tr>
    <td>Fx.crm.account.giveBack(&lt;String 客户Id&gt;, &lt;String 公海Id&gt;)</td>
    <td>客户退回公海</td>
    <td>Map</td>
  </tr>
  <tr>
    <td>Fx.crm.account.takeOut(&lt;List 客户Ids&gt;)</td>
    <td>客户领取</td>
    <td>Map</td>
  </tr>

<tr>
    <td rowspan="4" >Fx.work</td>
  </tr>

  <tr>
    <td>Fx.work.createTask(&lt;String title&gt;,&lt;String content&gt;,&lt;DateTime deadLine&gt;,&lt;Map&lt;List&gt; executeUsers&gt;, &lt;Map&lt;List&gt; atUsers&gt;) //**executeUsers**的key值 : "users" 用户 ，"departments" 部门；**atUsers**的key值 : "users" 用户 ，"departments" 部门</td>
    <td>发任务</td>
    <td>无</td>
  </tr>
  <tr>
    <td>Fx.work.createSchedule(&lt;String content&gt;,&lt;DateTime beginTime&gt;,&lt;DateTime endTime&gt;, &lt;boolean isFullDate&gt;,&lt;boolean needReceipt&gt;,&lt;List remindTimes&gt;,&lt;Map&lt;List&gt; atUsers&gt;) //atUsers的key值 : "users" 用户 ，"departments" 部门</td>
    <td>发日程</td>
    <td>无</td>
  </tr>
  <tr>
    <td>Fx.work.createSalesRecord(&lt;String content&gt;,&lt;Map objects&gt;,&lt;Map&lt;List&gt; atUsers&gt;) //objects的key值："object_api_name" 对象APIName , "id" 对象Id；atUsers的key值 : "users" 用户 ，"departments" 部门</td>
    <td>发销售记录</td>
    <td>无</td>
  </tr>


  <tr>
<td>Fx.random</td>
    <td>Fx.random.nextInt()或Fx.random.nextInt(&lt;Integer integer&gt;)</td>
    <td>生成随机数</td>
    <td>无</td>
  </tr>

<tr>
    <td rowspan="8" >Fx.crypto</td>
  </tr>

  <tr>
    <td>Fx.crypto.MD5.encode(&lt;String content&gt;)或Fx.crypto.MD5.encode(&lt;byte[] content&gt;)</td>
    <td>MD5加密</td>
    <td>String</td>
  </tr>
  <tr>
    <td>Fx.crypto.DESede.encode(&lt;byte[] key&gt;,&lt;String iv&gt;,&lt;byte[] data&gt;)</td>
    <td>DESede加密</td>
    <td>byte[ ]</td>
  </tr>
  <tr>
    <td>Fx.crypto.DESede.decode(&lt;byte[] key&gt;,&lt;String iv&gt;,&lt;byte[ ] data&gt;)</td>
    <td>DESede解密</td>
    <td>byte[ ]</td>
  </tr>
  <tr>
    <td>Fx.crypto.Base64.encode(&lt;byte[] data&gt;)</td>
    <td>Base64加密</td>
    <td>String</td>
  </tr>  <tr>
    <td>Fx.crypto.Base64.decode(&lt;String data&gt;)或Fx.crypto.Base64.decode(&lt;byte[] data&gt;)</td>
    <td>Base64解密</td>
    <td>byte[ ]</td>
  </tr>
  <tr>
    <td>Fx.crypto.SHA1.encode(&lt;String data&gt;)或Fx.crypto.SHA1.encode(&lt;byte[] data&gt;)</td>
    <td>SHA1API加密</td>
    <td>byte[ ]</td>
  </tr>
  <tr>
    <td>Fx.crypto.SHA1.hex(&lt;String data&gt;)或Fx.crypto.SHA1.hex(&lt;byte[] data&gt;)</td>
    <td>SHA1API十六进制</td>
    <td>byte[ ]</td>
  </tr>
<tr>
    <td rowspan="3" >Fx.json</td>
  </tr>

  <tr>
    <td>Fx.json.toJson(&lt;Map map&gt;)</td>
    <td>Map转json字符串</td>
    <td>String</td>
  </tr>
  <tr>
    <td>Fx.json.parse(&lt;String jsonstr&gt;)</td>
    <td>json转Map字符串</td>
    <td>Map</td>
 </tr>

<tr>
    <td rowspan="3" >Fx.location</td>
  </tr>

  <tr>
    <td>Fx.location.findByMobile(&lt;String mobile&gt;)</td>
    <td>查询单个号码归属地</td>
    <td>Map</td>
  </tr>
  <tr>
    <td>Fx.location.findByMobiles( [ List&lt;String&gt; mobiles ] )</td>
    <td>批量查询手机号归属地</td>
    <td>Map</td>
 </tr>
<tr>
    <td rowspan="3" >Fx.message</td>
  </tr>

  <tr>
    <td>Fx.message.send(String textMessage , List&lt;Integer&gt; receiverIds , &lt;Channel channel&gt;)</td>
    <td>发送文本消息</td>
    <td>String</td>
  </tr>
  <tr>
    <td>Fx.message.send(&lt;Card card&gt; ,  List&lt;Integer&gt;receiverIds; , &lt;Channel channel&gt;)</td>
    <td>发送卡片消息</td>
    <td>String</td>
 </tr>


  </table>



Fx.object.find方法中的条件语句如下（使用Operator.调用）：

| 说明             | 代码格式                   |
| ---------------- | -------------------------- |
| 判断相等         | EQ(&lt;Object str&gt;)     |
| 判断不相等       | NE(&lt;Object str&gt;)     |
| 判断大于         | GT(&lt;Object str&gt;)     |
| 判断小于         | LT(&lt;Object str&gt;)     |
| 判断大于等于     | GTE(&lt;Object str&gt;)    |
| 判断小于等于     | LTE(&lt;Object str&gt;)    |
| 判断是否包含     | LIKE(&lt;String str&gt;)   |
| 判断不包含       | NLIKE(&lt;String str&gt;)  |
| 判断属于其中一个 | IN(&lt;List str&gt;)       |
| 判断不属于其中   | NIN(&lt;List list&gt;)     |
| 判断字段是否有值 | EXISTS(&lt;boolean ex&gt;) |



