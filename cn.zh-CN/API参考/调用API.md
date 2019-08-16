# 调用API {#concept_1216491 .concept}

城市视觉智能引擎接口调用是向城市视觉智能引擎API的服务端地址发送HTTP GET请求，并按照接口说明在请求中加入相应请求参数，调用后系统会返回处理结果。请求及返回结果都使用UTF-8字符集进行编码。

## 请求结构 {#section_dav_jqb_v00 .section}

城市视觉智能引擎的API是RPC风格，您可以通过发送HTTP GET请求调用API。

其请求结构如下：

``` {#codeblock_zj8_435_u9b}
http://Endpoint/?Action=xx&Parameters
```

其中：

-   Endpoint： 城市视觉智能引擎API的服务接入地址为cityvisual.\[RegionId\].aliyuncs.com。
-   Action：要执行的操作，如调用DescribeInstances查询已创建的城市视觉智能引擎实例。
-   Version：要使用的API版本，城市视觉智能引擎的API版本是2018-10-30。
-   Parameters：请求参数，每个参数之间用“&”分隔。

    请求参数由公共请求参数和API自定义参数组成。公共参数中包含API版本号、身份验证等信息，详情请参见 [公共参数](cn.zh-CN/API参考/公共参数.md#)。


下面是一个调用DescribeInstances接口查询已创建的城市视觉智能引擎实例详细信息的示例：

**说明：** 为了便于用户查看，本文档中的示例都做了格式化处理。

``` {#codeblock_zw3_0mt_24q}
https://cityvisua.cn-shanghai.aliyuncs.com/?Action=DescribeInstances
&RegionId=cn-shanghai
&Format=JSON
&Version=2018-10-30
&Signature=xxxx%xxxx%3D
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396
&SignatureVersion=1.0
&AccessKeyId=key-test
&TimeStamp=2019-09-01T12:00:00Z
…
```

