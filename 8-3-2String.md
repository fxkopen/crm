# String类型


String - 字符串类型，使用时用""封装，中间可写任意字符（中文、英文、符号等）

定义String：`String string = ""`

例：

>     String string = "张三"

String类型的方法：

 - **string.contains(&lt;String str&gt;)**：判断字符串中是否包含特定序列或字符
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "fx is great".contains("fx") //返回：true


----------


 - **string.startsWith(&lt;String str&gt;)**：检测是否以特定字符串开头
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "fx is great".startsWith("fx") //返回：true


----------


 - **string.endsWith(&lt;String str&gt;)**：检测是否以特定字符串结尾
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "fx is great".endWith("fx") //返回：false


----------


 - **string.concat(&lt;String str&gt;)**：将制定的字符串加在此字符串的末尾
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "fx is great".concat("fx") //返回：fx is greatfx


----------


 - **string.isEmpty()**：判断是否为空
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：Boolean

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "fx ".isEmpty() //返回：false


----------


 - **string.trim()**：返回字符串的副本，忽略前导空白和尾部空白
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "  Welcome to fxiaoke Creator ".trim() //返回：Welcome to fxiaoke Creator


----------


 - **string.replace(&lt;String searchString&gt;,&lt;String replacement&gt;)**：使用给定的参数replacement替换字符串所有匹配给定的searchString的子字符串
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "Red,Green,Green".replace("Green","Blue") //返回：Red,Blue,Blue


----------


 - **string.replaceAll(&lt;String regex&gt;,&lt;String replacement&gt;)**：使用给定的参数replacement替换字符串所有匹配给定的regex(正则表达式)的子字符串
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "Red,Green,Green".replaceAll("Green","Blue") //返回：Red,Blue,Blue


----------


 - **string.substring(&lt;Integer startIndex&gt;,&lt;Integer endIndex&gt;)**：返回一个新字符串，它是此字符串中的一个子字符串
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：String

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "www.fxiaoke.com".substring(4,11) //返回：fxiaoke

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：在程序语言中，是从第0位开始的，所以上例中的第四位是f；最终返回的结果中包含startIndex，不包含endIndex


----------


 - **string.split(&lt;String regex&gt;) 或 string.split(&lt;String regex&gt;,&lt;Integer limit&gt;)**根据匹配给定的正则表达式来拆分字符串
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：List

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>      "www-fxiaoke-com".split("-") //返回：["www","fxiaoke","com"]

>      "www-fxiaoke-com".split("-","2") //返回：["www","fxiaoke-com"]

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注：在string.split(&lt;String regex&gt;,&lt;Integer limit&gt;)中limit表示将该字符串最多拆分成几个字符串


----------


 - **string.length()**返回此字符串的长度
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       "www.fxiaoke.com".length() //返回：15


----------


 - **string.indexOf(&lt;String subString&gt;)**返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引处开始（默认从0开始）

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;或**string.indexOf(&lt;String subString&gt;,&lt;SBigDecimal fromIndex&gt;)**返回指定子字符串在此字符串中从fromIndex后第一次出现处的索引，从指定的索引处开始（默认从0开始）
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       "www.fxiaoke.com".indexOf("o") //返回：8

>       "www.fxiaoke.com".indexOf("o"，9) //返回：13


----------


 - **string.lastIndexOf(&lt;String subString&gt;)**返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引处开始反向搜索

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;或** string.lastIndexOf(&lt;String subString&gt;,&lt;BigDecimal fromIndex&gt;)**返回指定子字符串在此字符串中在lastIndexOf前最后一次出现处的索引，从指定的索引处开始反向搜索
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;返回值类型：BigDecimal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;例：

>       "www.fxiaoke.com".indexOf("o") //返回：13

>       "www.fxiaoke.com".indexOf("o",9) //返回：8

