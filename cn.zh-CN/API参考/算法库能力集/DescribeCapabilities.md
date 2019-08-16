# DescribeCapabilities {#doc_api_cityvisual_DescribeCapabilities .reference}

调用DescribeCapabilities获取已创建的算法库能力集信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeCapabilities&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCapabilities|系统规定参数。取值：**DescribeCapabilities**。

 |
|InstanceId|String|是|cityvisual-xxxxx|实例ID。

 |
|PageNumber|Integer|否|1|算法库能力集列表的页码。起始值：1。

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
|Capabilities| | |算法库能力集集合。

 |
|CapabilityId|String|362|算法库能力集ID。

 |
|CapabilityName|String|PERSON|算法库能力集名称。

 |
|PageNumber|Integer|1|算法库能力集列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|TotalCount|Integer|100|获取到的能力集总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeCapabilities
&InstanceId=cityvisual-xxxxx
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCapabilitiesResponse>
      <Capabilities>
            <Capability>
                  <CapabilityId>xxxxx</CapabilityId>
                  <CapabilityName>PERSON</CapabilityName>
            </Capability>
      </Capabilities>
      <PageNumber>1</PageNumber>     
      <PageSize>10</PageSize>     
      <TotalCount>1</TotalCount>
      <RequestId>04F0F334-1335-436C-A1D7-6C044FE73368</RequestId>
</DescribeCapabilitiesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":1,
	"TotalCount":1,
	"PageSize":10,
	"RequestId":"04F0F334-1335-436C-A1D7-6C044FE73368",
	"Capabilities":{
		"Capability":[
			{
				"CapabilityName":"PERSON",
				"CapabilityId":"xxxxx"
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

