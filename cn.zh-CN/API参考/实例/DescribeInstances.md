# DescribeInstances {#doc_api_cityvisual_DescribeInstances .reference}

调用DescribeInstances查询一个或多个实例的详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeInstances&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstances|系统规定参数。取值：DescribeInstances。

 |
|RegionId|String|是|cn-hangzhou|实例所属的地域ID。您可以调用DescribeRegions查看最新的阿里云地域列表。

 |
|InstanceIds|String|否|\["cityvisual-xxxxxxxxx", "cityvisual-yyyyyyyyy", … "cityvisual-zzzzzzzzz"\]|实例ID。取值可以由多个实例ID组成一个JSON数组，最多支持100个ID，ID之间用半角逗号（,）隔开。

 |
|InstanceName|String|否|\*Joshua|实例名称，支持使用通配符\*进行模糊搜索。

 |
|PageNumber|Integer|否|1|实例状态列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Instances| | |实例列表

 |
|CreateTime|String|2018-10-10T10:20:30Z|创建时间

 |
|Description|String|description|实例描述

 |
|InstanceCapacity|Integer|2|接流路数

 |
|InstanceId|String|cityvisual-instanceid1|实例ID

 |
|InstanceName|String|FinanceJoshua|实例名称

 |
|RegionId|String|cn-hangzhou|实例所属地域ID。

 |
|Status|String|Running|实例状态，取值范围：

 -   Running 运行中
-   Stopped 已停止

 |
|PageNumber|Integer|1|实例列表的页码。

 |
|PageSize|Integer|10|输入时设置的每页行数。

 |
|RequestId|String|7D800EB6-8565-47EC-87B2-213960F77508|请求ID

 |
|TotalCount|Integer|200|实例总数

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeInstances
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeInstancesResponse>
    <PageNumber>1</PageNumber>
    <TotalCount>20</TotalCount>
    <PageSize>10</PageSize>
    <RequestId>14A07460-EBE7-47CA-9757-12CC4761D47A</RequestId>
    <Instances>
        <Instance>
            <InstanceId>cityvisual-instanceid1</InstanceId>
            <InstanceName>FinanceJoshua</InstanceName>
            <InstanceCapacity>10</InstanceCapacity>
            <Description></Description>
            <CreateTime>2015-07-27T07:08Z</CreateTime>
            <Status>Running</Status>
            <RegionId>cn-shanghai</RegionId>
        </Instance>
    </Instances>
</DescribeInstancesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":"1",
	"TotalCount":"20",
	"PageSize":"10",
	"RequestId":"14A07460-EBE7-47CA-9757-12CC4761D47A",
	"Instances":{
		"Instance":[
			{
				"Status":"Running",
				"Description":"",
				"RegionId":"cn-shanghai",
				"CreateTime":"2015-07-27T07:08Z",
				"InstanceId":"cityvisual-instanceid1",
				"InstanceCapacity":10,
				"InstanceName":"FinanceJoshua"
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

