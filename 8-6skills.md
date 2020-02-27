# 使用技巧

####1. 如何获取对象和字段的API？

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;登录Web端纷享销客，进入【管理】频道，打开【定制化开发】选项下的【对象及字段API】页面，即所有对象及每个对象的字段API Name都会在此显示，点击API Name后面的复制图标，可一键复制到函数编辑器内
 ![对象及字段API.png-337.8kB][1]
 
####2. 如何获取对象实例的ID？
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• 在要查找的对象列表页右键后点击【检查】，进入开发模式

 ![对象ID步骤1.png-157.7kB][2]
 
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• 在开发模式中切换到【Network】下然后在左侧页面下点击要查找的对象实例，如下图点击张大三
 
 ![对象ID步骤2.png-128kB][3]
 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• 发现在开发模式下动态加载了很多文件，找到Detail开头的文件
 
 ![对象ID步骤3.png-129kB][4]
 
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• 在右侧找到Value下的data数据下加载了所有该联系人的参数信息
 
 ![对象ID步骤4.png-210.5kB][5]
 
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• 在下面即可找到_id即为张大三这个联系人的ID
 ![对象ID步骤5.png-203.7kB][6]

 
  [1]: http://static.zybuluo.com/BanGongGroup/us64kebmzo9skjadsv6rjuue/%E5%AF%B9%E8%B1%A1%E5%8F%8A%E5%AD%97%E6%AE%B5API.png
  [2]: http://static.zybuluo.com/BanGongGroup/1dhi06pn6jylfirvv72uw6j5/%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A41.png
  [3]: http://static.zybuluo.com/BanGongGroup/d6z472bknhxq9wgr1hmsgoiw/%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A42.png
  [4]: http://static.zybuluo.com/BanGongGroup/r1oa6b5aq93lh943yle5y8pf/%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A43.png
  [5]: http://static.zybuluo.com/BanGongGroup/wcmtws1kuece91xzbzlakug3/%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A44.png
  [6]: http://static.zybuluo.com/BanGongGroup/w6qiim1x14616wuaqv1hfjp3/%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A45.png
  [7]: http://static.zybuluo.com/BanGongGroup/eakapyg1sdcx3yqkk68otk1k/%E7%AE%A1%E7%90%86%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A41.png
  [8]: http://static.zybuluo.com/BanGongGroup/8qngnyj3u14g4ryq4ad7arur/%E7%AE%A1%E7%90%86%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A42.png
  [9]: http://static.zybuluo.com/BanGongGroup/niq4ha8z7v8jujs9k9xe933c/%E7%AE%A1%E7%90%86%E5%AF%B9%E8%B1%A1ID%E6%AD%A5%E9%AA%A43.png