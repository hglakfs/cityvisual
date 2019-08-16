# DescribeResourceProfiles {#doc_api_cityvisual_DescribeResourceProfiles .reference}

调用DescribeResourceProfiles获取已创建的计算资源配置信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeResourceProfiles&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeResourceProfiles|系统规定参数。取值：**DescribeResourceProfiles**。

 |
|InstanceId|String|是|cityvisual-Instance|实例ID。

 |
|PageNumber|Integer|是|1|资源参数集列表的页码。起始值：**1**。

 默认值：**1** 。

 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。最大值：**100**。

 默认值：**10**。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |
|ResourceProfileId|String|否|3|资源参数集ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNumber|Integer|1|计算资源配置信息列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|ResourceProfiles| | |计算资源参数信息。

 |
|ResourceProfileId|String|6|计算资源参数信息ID。

 |
|ResourceProfileName|String|name|计算资源参数信息名称。

 |
|ResourceProfileParams| | |计算资源参数信息参数。

 |
|Key|String|MQ\_NAMESERVERS|资源参数的键，取值范围：

 \* MQ\_NAMESERVERS

 \* MQ\_TOPIC

 \* MQ\_GROUP

 \* MQ\_TIMESTAMP\_PRE\_SEC

 \* OSS\_ENDPOINT

 \* OSS\_PUB\_ENDPOINT

 \* OSS\_ACCESSKEYID

 \* OSS\_ACCESSKEYSECRET

 \* OSS\_BUCKET

 \* ES\_ADDRESS

 \* ES\_CLUSTERNAME

 \* ES\_PERSON\_INDEX

 \* ES\_NOVEHICLE\_INDEX

 \* ES\_VEHICLE\_INDEX

 \* RDS\_HOSTNAME

 \* RDS\_DBNAME

 \* RDS\_PERSON\_TABLE

 \* RDS\_NOVEHICLE\_TABLE

 \* RDS\_VEHICLE\_TABLE

 \* RDS\_USER

 \* RDS\_PASSWORD

 |
|Value|String|xxx|资源参数的值。

 |
|TotalCount|Integer|200|计算资源参数信息总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeResourceProfiles
&InstanceId=cityvisual-Instance
&PageNumber=1
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeResourceProfilesResponse>
      <ResourceProfiles>
            <ResourceProfile>
                  <ResourceProfileId>xxxxx</ResourceProfileId>
                  <ResourceProfileName>Global Resource Profile</ResourceProfileName>
                  <ResourceProfileParams>		
                        <ResourceProfileParam>
                              <Key>MQ_NAMESERVERS</Key>
                              <Value>192.168.100.100:9300</Value>
                        </ResourceProfileParam>
                        <ResourceProfileParam>
                              <Key>MQ_GROUP</Key>
                              <Value>ConsumerGroup1</Value>
                        </ResourceProfileParam>
                  </ResourceProfileParams>
            </ResourceProfile>
      </ResourceProfiles>
      <PageNumber>1</PageNumber>     
      <PageSize>10</PageSize>     
      <TotalCount>1</TotalCount>
      <RequestId>04F0F334-1335-436C-A1D7-6C044FE73368</RequestId>
</DescribeResourceProfilesResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":1,
	"TotalCount":1,
	"ResourceProfiles":{
		"ResourceProfile":[
			{
				"ResourceProfileId":"xxxxx",
				"ResourceProfileParams":{
					"ResourceProfileParam":[
						{
							"Value":"192.168.100.100:9300",
							"Key":"MQ_NAMESERVERS"
						},
						{
							"Value":"ConsumerGroup1",
							"Key":"MQ_GROUP"
						}
					]
				},
				"ResourceProfileName":"Global Resource Profile"
			}
		]
	},
	"PageSize":10,
	"RequestId":"04F0F334-1335-436C-A1D7-6C044FE73368"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

