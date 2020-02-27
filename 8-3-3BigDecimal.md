# BigDecimal类型

BigDecimal - 数字类型

定义BigDecimal：`BigDecimal b`

例：

>     BigDecimal b = 0.01

BigDecimal类型的静态方法：

 - **BigDecimal.of(&lt;String value&gt;)**
 - **BigDecimal.of(&lt;Number value&gt;)**

保留小数：

- **b.setScale(小数位数,BigDecimal.ROUND_HALF_UP)   四舍五入**

- **b.setScale(小数位数,BigDecimal.ROUND_HALF_DOWN)   直接截取**

例：

> BigDecimal test = BigDecimal.of("1.66666")
> test.setScale(2,BigDecimal.ROUND_HALF_UP)//保留两位小数四舍五入 1.67
> test.setScale(2,BigDecimal.ROUND_HALF_DOWN);//保留两位小数直接截取  1.66