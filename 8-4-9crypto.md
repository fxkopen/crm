# Fx.crypto

Fx.crypto：和加解密相关的API
####1、MD5 加密-MD5
 - **定义**：Fx.crypto.MD5.encode(&lt;String content&gt;)
 &nbsp;&nbsp;&nbsp;或：Fx.crypto.MD5.encode(&lt;byte[] content&gt;)

 - **data返回值类型**：String
 - **举例**：
 >      Fx.crypto.MD5.encode("fxiaoke")
 
 >      Fx.crypto.MD5.encode([1,2] as byte[])
 
----------

####2、DESede加密-DESede
 - **加密**：Fx.crypto.DESede.encode(&lt;byte[] key&gt;,&lt;String iv&gt;,&lt;byte[] data&gt;)

   **data返回值类型**：byte[ ]

参数 |说明|
-|-
key | 加密秘钥
iv | 初始向量
data | 加密数据

   **举例**：
 
 >      Fx.crypto.DESede.encode(Strings.toUTF8Bytes("123456789101112131415123116") ,"12345678",[1,2] as byte[])

 - **解密**：Fx.crypto.DESede.decode(&lt;byte[] key&gt;,&lt;String iv&gt;,&lt;byte[ ] data&gt;)

 **data返回值类型**：byte[ ]

参数 |说明|
-|-
key | 加密秘钥
iv | 初始向量
data | 加密数据

  **举例**：
 
 >      Fx.crypto.DESede.decode(Strings.toUTF8Bytes("123456789101112131415123116") ,"12345678",[1,2] as byte[ ])


----------
####3、Base64 加解密-Base64
 - **加密**：Fx.crypto.Base64.encode(&lt;byte[] data&gt;)

 **data返回值类型**：String

 **举例**：
 
 >      Fx.crypto.Base64.encode([1] as byte[])
 
 - **解密**：Fx.crypto.Base64.decode(&lt;String data&gt;)
 &nbsp;&nbsp;&nbsp;或：Fx.crypto.Base64.decode(&lt;byte[] data&gt;)

 **data返回值类型**：byte[]

 **举例**：
 
 >      Fx.crypto.Base64.decode("content")
 
 >      Fx.crypto.Base64.decode([1,2] as byte[])
 


----------


#### 4、SHA1API 加解密-SHA1
 - **加密**：Fx.crypto.SHA1.encode(&lt;String data&gt;)
  &nbsp;&nbsp;&nbsp;或：Fx.crypto.SHA1.encode(&lt;byte[] data&gt;)

 **data返回值类型**：byte[]

 **举例**：
 
 >     Fx.crypto.SHA1.encode("data") 
 >     Fx.crypto.SHA1.encode([1,2] as byte[])
 
 - **十六进制**：Fx.crypto.SHA1.hex(&lt;String data&gt;)
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;或：Fx.crypto.SHA1.hex(&lt;byte[] data&gt;)

 **data返回值类型**：byte[]

 **举例**：
 
 >      Fx.crypto.SHA1.hex("data")
 
 >      Fx.crypto.SHA1.hex([1,2] as byte[])


