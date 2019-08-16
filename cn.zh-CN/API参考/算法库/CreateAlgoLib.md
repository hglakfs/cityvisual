# CreateAlgoLib {#doc_api_cityvisual_CreateAlgoLib .reference}

调用CreateAlgoLib创建算法库。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=CreateAlgoLib&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateAlgoLib|系统规定参数。取值：**CreateAlgoLib**。

 |
|AlgoLibName|String|是|name|算法库名称。

 |
|AlgoLibVersion|String|是|1.0.0|算法库版本。

 |
|CapabilityNames|String|是|PERSON,FACE|能力集名称，多个能力集用半角“,”隔开。

 |
|Capacity|Integer|是|30|算法库计算容量，对应视频路数。

 |
|InstanceId|String|是|cityvisual-\*\*\*\*|实例ID。

 |
|JsonText|String|是|\[\{ "objType": "person", "dbTableName": "person\_offline\_result", "indexName": "person\_offline\_index", "indexMode": "INDEX\_PER\_DAY", "topicName": "person\_offline", "fields": \[\{ "name": "cameraId", "type": "string", "mandatory": true, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \}, \{ "name": "objType", "type": "string", "mandatory": true, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \}, \{ "name": "fileId", "type": "string", "mandatory": false, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \} \] \}\]|算法库配置参数，Json格式的字符串。

 |
|OssAccessKeyId|String|是|LTAI\*\*\*\*\*\*\*\*CSXJ|算法包所在OSS的AccessKey ID。

 |
|OssAccessKeySecret|String|是|etyDr0EZnf9NQ\*\*\*\*\*\*\*\*\*\*\*\*\*isN0|算法包所在OSS的AccessKey Secret。

 |
|OssBucket|String|是|bucket|算法包所在OSS的存储空间Bucket名称。

 |
|OssEndpoint|String|是|oss-cn-shanghai-internal.aliyuncs.com|算法包所在OSS的Endpoint。

 |
|OssPath|String|是|library/xxxx.tar.gz|算法包在OSS中的相对路径。

 |
|Text|String|是|xxx|算法库的配置信息，jsonText的文本形式。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|AlgoLibId|String|36|创建的算法库ID。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateAlgoLib
&AlgoLibName=name
&AlgoLibVersion=1.0.0
&CapabilityNames=PERSON,FACE
&Capacity=30
&InstanceId=cityvisual-****
&JsonText=[{      "objType": "person",      "dbTableName": "person_offline_result",      "indexName": "person_offline_index",      "indexMode": "INDEX_PER_DAY",      "topicName": "person_offline",      "fields": [{          "name": "cameraId",          "type": "string",          "mandatory": true,          "isDatabaseField": true,          "isSearchEngineField": true,          "isMessageQueueField": true      }, {          "name": "objType",          "type": "string",          "mandatory": true,          "isDatabaseField": true,          "isSearchEngineField": true,          "isMessageQueueField": true      }, {          "name": "fileId",          "type": "string",          "mandatory": false,          "isDatabaseField": true,          "isSearchEngineField": true,          "isMessageQueueField": true      }  ]  }]
&OssAccessKeyId=LTAI********CSXJ
&OssAccessKeySecret=etyDr0EZnf9NQ*************isN0
&OssBucket=bucket
&OssEndpoint=oss-cn-shanghai-internal.aliyuncs.com
&OssPath=library/xxxx.tar.gz
&Text=xxx
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateAlgoLibResponse>
      <AlgoLibId>36</AlgoLibId>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</CreateAlgoLibResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"AlgoLibId":36,
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|400|InvalidName.Malformed|The specified Name is incorrectly formatted.|指定的Name格式不合法。|
|404|InvalidOssBucket.NotFound|The specified OssBucket does not exist.|指定的OssBucket不存在。|
|403|InvalidOssBucket.ValueUnauthorized|You are not authorized to operate on the specified OSS bucket.|指定OssBucket无权限。|
|404|InvalidOssEndpoint.NotFound|The specified OssEndpoint does not exist.|指定的OssEndpoint不存在。|
|400|InvalidCapacity.ValueNotSupported|The specified Capacity is invalid.|指定的Capacity不合法。|
|400|InvalidCapabilities.ValueNotSupported|The specified Capabilities is invalid.|指定的Capabilities不合法。|
|400|InvalidName.Duplicate|The specified name already exists.|指定的名称已存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

