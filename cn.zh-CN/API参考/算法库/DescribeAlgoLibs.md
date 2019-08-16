# DescribeAlgoLibs {#doc_api_cityvisual_DescribeAlgoLibs .reference}

调用DescribeAlgoLibs获取已创建的算法库信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeAlgoLibs&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlgoLibs|系统规定参数。取值：**DescribeAlgoLibs**。

 |
|InstanceId|String|是|351|实例ID。

 |
|AlgoLibId|String|否|372|算法库ID。

 |
|AlgoLibName|String|否|name|算法库名称。

 |
|CapabilityName|String|否|PERSON,FACE|算法库能力集，多个能力集用半角“,”隔开。

 |
|PageNumber|Integer|否|1|算法库列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|AlgoLibs| | |算法库。

 |
|AlgoLibId|String|xxxxx|算法库ID。

 |
|AlgoLibName|String|person-face|算法库名称。

 |
|AlgoLibVersion|String|1.0.0|算法库版本。

 |
|CapabilityNames|String|PERSON,FACE|能力集名称。

 |
|Capacity|String|30|算法库计算容量，对应视频路数。指定该参数后，其取值范围必须是`[1，50]`。

 |
|JsonText|String|\[\{ "objType": "person", "dbTableName": "person\_offline\_result", "indexName": "person\_offline\_index", "indexMode": "INDEX\_PER\_DAY", "topicName": "person\_offline", "fields": \[\{ "name": "cameraId", "type": "string", "mandatory": true, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \}, \{ "name": "objType", "type": "string", "mandatory": true, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \}, \{ "name": "fileId", "type": "string", "mandatory": false, "isDatabaseField": true, "isSearchEngineField": true, "isMessageQueueField": true \} \] \}\]|Json格式的字符串。

 |
|OssAccessKeyId|String|LTAI\*\*\*\*\*\*\*\*CSXJ|算法包所在OSS的AccessKey ID。

 |
|OssBucket|String|bucket|算法包所在OSS的存储空间Bucket名称。

 |
|OssEndpoint|String|oss-cn-shanghai-internal.aliyuncs.com|算法包所在OSS的Endpoint。

 |
|OssPath|String|library/xxxx.tar.gz|算法包在OSS中的相对路径。

 |
|Text|String|xxx|算法库配置信息。

 |
|UploadTime|String|2018-10-10T10:20:30Z|上传时间。

 |
|PageNumber|Integer|1|算法库列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|14A07460-EBE7-47CA-9757-12CC4761D47A|请求ID。

 |
|TotalCount|Integer|200|当前实例下的算法库总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAlgoLibs
&InstanceId=351
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAlgoLibsResponse>
      <AlgoLibs>
            <AlgoLib>
                  <AlgoLibName>Video compute library</AlgoLibName>
                  <AlgoLibVersion>1.2.34</AlgoLibVersion>
                  <CapabilityNames>PERSON,FACE</CapabilityNames>
                  <Capacity>15</Capacity>
                  <OssEndpoint> 
                oss-cn-shanghai-internal.aliyuncs.com 
            </OssEndpoint>
                  <OssAccessKeyId> xxxxxxxxxx </OssAccessKeyId>
                  <OssBucket>tq-library-bucket </OssBucket>
                  <OssPath>lib/VideoProcessor.tgz</OssPath>
            </AlgoLib>
	        <AlgoLib>
                  <AlgoLibName>Video compute test library</AlgoLibName>
                  <AlgoLibVersion>1.2.35</AlgoLibVersion>
                  <CapabilityNames>PERSON,FACE</CapabilityNames>
                  <Capacity>15</Capacity>
                  <OssEndpoint> 
                oss-cn-shanghai-internal.aliyuncs.com 
            </OssEndpoint>
                  <OssAccessKeyId> xxxxxxxxxx </OssAccessKeyId>
                  <OssBucket>tq-library-bucket </OssBucket>
                  <OssPath>lib/VideoProcessorTest.tgz</OssPath>
	        </AlgoLib>
      </AlgoLibs>
      <PageNumber>1</PageNumber>     
      <PageSize>10</PageSize>     
      <TotalCount>2</TotalCount>
      <RequestId>04F0F334-1335-436C-A1D7-6C044FE73368</RequestId>
</DescribeAlgoLibsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":1,
	"TotalCount":2,
	"PageSize":10,
	"RequestId":"04F0F334-1335-436C-A1D7-6C044FE73368",
	"AlgoLibs":{
		"AlgoLib":[
			{
				"OssPath":"lib/VideoProcessor.tgz",
				"AlgoLibVersion":"1.2.34",
				"AlgoLibName":"Video compute library",
				"OssEndpoint":"oss-cn-shanghai-internal.aliyuncs.com",
				"CapabilityNames":"PERSON,FACE",
				"OssBucket":"tq-library-bucket",
				"Capacity":15,
				"OssAccessKeyId":"xxxxxxxxxx"
			},
			{
				"OssPath":"lib/VideoProcessorTest.tgz",
				"AlgoLibVersion":"1.2.35",
				"AlgoLibName":"Video compute test library",
				"OssEndpoint":"oss-cn-shanghai-internal.aliyuncs.com",
				"CapabilityNames":"PERSON,FACE",
				"OssBucket":"tq-library-bucket",
				"Capacity":15,
				"OssAccessKeyId":"xxxxxxxxxx"
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

