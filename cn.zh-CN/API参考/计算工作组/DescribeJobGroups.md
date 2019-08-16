# DescribeJobGroups {#doc_api_cityvisual_DescribeJobGroups .reference}

调用DescribeJobGroups获取已创建的计算工作组信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=DescribeJobGroups&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeJobGroups|系统规定参数。取值：**DescribeJobGroups**。

 |
|InstanceId|String|是|cityvisual-Instance|实例ID。

 |
|PageNumber|Integer|是|1|计算工作组列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|是|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|JobGroupId|String|否|4|计算工作组ID。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|JobGroups| | |计算工作组。

 |
|AlgoLibId|String|xxxxxx|算法库ID。

 |
|ComputeJobs| | |计算工作组下的计算job。

 |
|ComputeJobId|String|62|Job的ID。

 |
|ComputeJobName|String|jobName|Job的名称。

 |
|ComputeJobStatus|String|Running|Job的状态。取值范围：

 \* Running: 运行中

 \* Stopped: 已停止

 |
|Duration|Integer|1000|已经启动的时间。

 |
|EndTime|String|2018-10-10T11:20:30Z|停止时间。

 |
|StartTime|String|2018-10-10T10:20:30Z|启动时间。

 |
|JobCount|Integer|10|Job总数。

 |
|JobGroupId|String|daj28d89edh8|JobGroup的ID。

 |
|JobGroupName|String|JobGroupName|JobGroup的名称。

 |
|JobGroupParams| | |由JobGroupParam组成的数组格式，返回计算工作组参数信息。

 |
|Key|String|ES\_ENABLE|JobGroup参数的键，取值范围：

 \* ES\_ENABLE: 结果输出到ES

 \* RDS\_ENABLE: 结果输出到RDS

 \* OUT\_MQ\_ENABLE: 结果输出到MQ

 \* DATAHUB\_ENABLE: 结果输出到DataHub

 \* SCHEDULE\_FLOW\_START\_TIME: 调度开始时间

 |
|Value|String|True|JobGroup参数的值。

 当参数键为**\_ENABLE时,取值范围: \* True: 输出 \* False: 不输出 当参数键为SCHEDULE\_FLOW\_START\_TIME时,取值范围: \* Latest: 最新 \* Oldest: 最旧**

 |
|PlanedJobCount|Integer|10|期望的Job数量。

 |
|ResourceProfileId|String|yjsadaid8q8wdw|资源参数集ID。

 |
|Status|String|Running|计算工作组状态。取值范围：

 \* starting: 启动中

 \* running: 运行中

 \* stopping: 停止中

 \* stopped: 已停止

 |
|StreamPerJob|Integer|4|Job下的视频流数量。

 |
|PageNumber|Integer|1|计算工作组列表的页码。起始值：1。

 默认值：1 。

 |
|PageSize|Integer|10|分页查询时设置的每页行数。最大值：100。

 默认值：10。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |
|TotalCount|Integer|200|该实例下的所有JobGroup。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeJobGroups
&InstanceId=cityvisual-Instance
&PageNumber=1
&PageSize=10
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeJobGroupsResponse>
      <JobGroups>
            <JobGroup>
                  <JobGroupId>xxxx</JobGroupId>
                  <Name>视频任务</Name>
                  <AlgoLibId>xxxxx</AlgoLibId>
                  <ResourceProfileId>xxxxx</ResourceProfileId>
                  <PlanedJobCount>10</PlanedJobCount>
                  <StreamPerJob>20</StreamPerJob>
                  <Status>running</Status>
                  <JobCount>10</JobCount>
                  <JobGroupParams>		
                        <JobGroupParam>
                              <Key>ES_ENABLE</Key>
                              <Value>True</Value>
                        </JobGroupParam>
                        <JobGroupParam>
                              <Key>RDS_ENABLE</Key>
                              <Value>True</Value>
                        </JobGroupParam>
                  </JobGroupParams>
                  <ComputeJobs>		
                        <ComputeJobId>101</ComputeJobId>
                        <ComputeJobName>101</ComputeJobName>
                        <ComputeJobStatus>Running</ComputeJobStatus>
                        <StartTime>2018-10-10T10:20:20Z</StartTime>
                        <EndTime>2018-10-10T10:20:30Z</EndTime>
                        <Duration>600</Duration>
                  </ComputeJobs>
            </JobGroup>
      </JobGroups>
      <PageNumber>1</PageNumber>     
      <PageSize>10</PageSize>     
      <TotalCount>1</TotalCount>
      <RequestId>04F0F334-1335-436C-A1D7-6C044FE73368</RequestId>
</DescribeJobGroupsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":1,
	"TotalCount":2,
	"JobGroups":{
		"JobGroup":[
			{
				"Name":"视频任务",
				"Status":"running",
				"AlgoLibId":"xxxxx",
				"ComputeJobs":[
					{
						"ComputeJobName":101,
						"ComputeJobId":101,
						"Duration":600,
						"EndTime":"2018-10-10T10:30:30Z",
						"StartTime":"2018-10-10T10:20:30Z",
						"ComputeJobStatus":"Running"
					}
				],
				"StreamPerJob":20,
				"JobGroupParams":{
					"JobGroupParam":[
						{
							"Value":"True",
							"Key":"ES_ENABLE"
						},
						{
							"Value":"True",
							"Key":"RDS_ENABLE"
						}
					]
				},
				"JobGroupId":"xxxxx",
				"JobCount":1,
				"ResourceProfileId":"xxxxx",
				"PlanedJobCount":1
			}
		]
	},
	"PageSize":10,
	"RequestId":"04F0F334-1335-436C-A1D7-6C044FE73368"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

