# 使用步骤


#### 1、新建编辑自定义函数

&nbsp;&nbsp;&nbsp;&nbsp;打开【管理】-【定制开发平台】-【自定义函数】界面，可进行新建或编辑自定义函数，还可从指定场景下执行自定义函数，具体参考应用场景

![函数列表.png-140.1kB][1]

&nbsp;&nbsp;&nbsp;&nbsp;新建自定义函数

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![自定义函数.png-34.5kB][2]

参数 |说明|
-|-
函数名称 | 设置函数的名称，以便使用时可以快速知道函数功能
Api Name | 该自定义函数的Api Name，方便后期查找使用
命名空间 | 命名空间可以理解为自定义函数的使用场景，可参考应用场景
返回值类型 | 根据命名空间的变化而不同，其中流程和促销默认值不可修改
绑定对象 | 设置函数要绑定的对象，以便于函数操作或获取绑定对象的属性字段
描述 | 描述所编写的自定义函数


----------






#### 2、函数编辑器

&nbsp;&nbsp;&nbsp;&nbsp;在函数编辑器中，可以添加函数脚本进行功能实现逻辑编写
![函数编辑.png-91kB][3]

 - 快捷插入：快捷向函数编辑区域插入代码

 - 放大编辑窗口：使函数编辑器窗口全屏展示

 - 设置参数：
![设置参数.png-28kB][4]

参数 |说明|
-|-
类型（必填） | 即参数的数据类型（String、BigDecimal、Boolean、DateTime、Date、Time）
名称（必填） | 参数的名称（必须满足命名规范）
默认值 | 参数默认值
显示名称 | 在使用函数绑定参数时的显示名称


 - 函数编辑页面：即编写函数代码区

 - 运行脚本：输出运行日志，包括返回值和运行错误提示

 - 选择数据源：可选择在新建函数时关联对象的任一实例数据并作为数据源

 ----------

 #### 3、自定义函数管理
 ![列表页.png-140.1kB][5]
 
&nbsp;&nbsp;&nbsp;&nbsp;1、可以查看自定义函数的相关信息，包括：函数名称、APIName、命名空间、绑定对象、返回值类型、创建时间、调用方、状态和可以进行的操作等；

&nbsp;&nbsp;&nbsp;&nbsp;2、可以根据命名空间和绑定对象筛选出对象的自定义函数，也可根据函数名称快速查找出对应的自定义函数；

&nbsp;&nbsp;&nbsp;&nbsp;3、可以进行新建、编辑和禁用自定义函数，自定义函数只有禁用后才能删除；

&nbsp;&nbsp;&nbsp;&nbsp;4、已经被使用的自定义函数会展示出调用方是按钮还是流程，并且无法在管理页面进行操作，只能在调用方进行编辑或解除关系


  [1]: http://static.zybuluo.com/BanGongGroup/72odnar0dmp4e7f39zugny4z/%E5%87%BD%E6%95%B0%E5%88%97%E8%A1%A8.png
  [2]: http://static.zybuluo.com/BanGongGroup/lt1nqbjnv0taikohqljze5gp/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0.png
  [3]: http://static.zybuluo.com/BanGongGroup/3ti5rbl8whr1extx5919ljyy/%E5%87%BD%E6%95%B0%E7%BC%96%E8%BE%91.png
  [4]: http://static.zybuluo.com/BanGongGroup/7ujy64t1ijvr6at2o9uzqkfs/%E8%AE%BE%E7%BD%AE%E5%8F%82%E6%95%B0.png
  [5]: http://static.zybuluo.com/BanGongGroup/eb1vzy99klftcxmcifr6u3fo/%E5%88%97%E8%A1%A8%E9%A1%B5.png