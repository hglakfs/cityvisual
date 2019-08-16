# DescribeStreams {#doc_api_cityvisual_DescribeStreams .reference}

调用DescribeStreams获取指定的计算工作组已绑定的视频流。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeStreams&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeStreams|系统规定参数。取值：**DescribeStreams**。

 |
|JobGroupId|String|是|51|关联的计算工作组ID。

 |
|PageNumber|Integer|否|1|视频流列表的页码。起始值：1。

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
|PageNumber|Integer|1|视频流列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|Streams| | |视频流。

 |
|ComputeJobId|String|35|Job的ID。

 |
|DelayMS|Integer|100|延迟，单位为ms。

 |
|JobGroupId|Integer|51|关联JobGroup的ID。

 |
|ObjCount|Integer|100|Obj数量。

 |
|StreamName|String|StreamName|视频流的名称。

 |
|StreamURL|String|mq://IP/...|流URL。

 |
|TotalCount|Integer|200|该实例下的视频流总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeStreams
&JobGroupId=51
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeStreamsResponse>
    <PageNumber>1</PageNumber>
    <TotalCount>1</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>14A07460-EBE7-47CA-9757-12CC4761D47A</RequestId>
    <Streams>
        <Stream>
            <DelayMS>100</DelayMS>
            <JobGroupId>51</JobGroupId>
            <JobId>3214</JobId>
            <StreamName>StreamName</StreamName>
            <ObjCount>100</ObjCount>
            <StreamURL>mq://IP/...</StreamURL>
        </Stream>
    </Streams>
</DescribeStreamsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":"1",
	"TotalCount":"1",
	"PageSize":"10",
	"RequestId":"14A07460-EBE7-47CA-9757-12CC4761D47A",
	"Streams":{
		"Stream":[
			{
				"StreamName":"StreamName",
				"JobGroupId":"51",
				"DelayMS":"100",
				"JobId":"3214",
				"ObjCount":"100",
				"StreamURL":"mq://IP/..."
			}
		]
	}
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidJobGroupId.NotFound|The specified job group does not exist.|指定的JobGroup不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

