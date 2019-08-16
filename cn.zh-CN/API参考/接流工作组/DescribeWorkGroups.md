# DescribeWorkGroups {#doc_api_cityvisual_DescribeWorkGroups .reference}

调用DescribeWorkGroups获取已创建的接流工作组。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeWorkGroups&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeWorkGroups|系统规定参数。取值：**DescribeWorkGroups**。

 |
|InstanceId|String|是|cityvisual-Instance|实例ID。

 |
|PageNumber|Integer|否|1|接流工作组列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|WorkGroupId|String|否|87|接流工作组ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNumber|Integer|1|工作组列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|TotalCount|Integer|200|该实例下的接流工作组总数。

 |
|WorkGroups| | |接流工作组集合。

 |
|CreateTime|String|2018-10-10T10:20:30Z|创建工作组的时间。

 |
|Description|String|描述信息|工作组描述信息。

 |
|InstanceId|String|xxx|实例ID。

 |
|Protocol|String|RTMP|协议。

 |
|TheoryCutStatus|String|False|视频调度状态。取值范围

 -   **True**: 参与视频调度
-   **False**: 不参与视频调度

 |
|UpdateTime|String|2018-11-10T10:20:30Z|最后一次修改的时间。

 |
|WorkGroupId|String|3274|接流工作组ID。

 |
|WorkGroupName|String|WorkGroupName|接流工作组名称。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeWorkGroups
&InstanceId=cityvisual-Instance
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeWorkGroupsResponse>
    <PageNumber>1</PageNumber>
    <TotalCount>1</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>14A07460-EBE7-47CA-9757-12CC4761D47A</RequestId>
    <WorkGroups>
        <WorkGroup>
            <CreateTime>2017-12-10T04:04Z</CreateTime>
            <Description>description</Description>
            <WorkGroupName>MyGroup</WorkGroupName>
            <ProtocolType>RTMP</ProtocolType>
            <WorkGroupId>3274</WorkGroupId>
            <UpdateTime>2015-07-27T07:08Z</UpdateTime>
            <TheoryCutStatus>False</TheoryCutStatus>
        </WorkGroup>
    </WorkGroups>
</DescribeWorkGroupsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":"1",
	"TotalCount":"1",
	"PageSize":"10",
	"RequestId":"14A07460-EBE7-47CA-9757-12CC4761D47A",
	"WorkGroups":{
		"WorkGroup":[
			{
				"Description":"description",
				"ProtocolType":"RTMP",
				"CreateTime":"2017-12-10T04:04Z",
				"TheoryCutStatus":"False",
				"UpdateTime":"2017-12-10T04:04Z",
				"WorkGroupId":"3274",
				"WorkGroupName":"MyGroup"
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

