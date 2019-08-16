# ListComputeJobLogs {#doc_api_cityvisual_ListComputeJobLogs .reference}

调用ListComputeJobLogs获取计算日志名称列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=cityvisual&api=ListComputeJobLogs&type=RPC&version=2018-10-30)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListComputeJobLogs|系统规定参数。取值：**ListComputeJobLogs**。

 |
|ComputeJobId|String|是|173|计算工作组下指定计算Job的ID。

 |
|JobGroupId|String|是|63|计算工作组ID。

 |
|RegionId|String|否|cn-shanghai|地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|JobLogs| |\[aaa.log,bbb.log\]|计算日志名称列表。

 |
|RequestId|String|E175B041-75A2-4335-B3AC-0FD008F93627|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=ListComputeJobLogs
&ComputeJobId=173
&JobGroupId=63
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ListComputeJobLogsResponse>
      <JobLogs>
            <JobLog>
            aaa.log,
            bbb.log
        </JobLog>
      </JobLogs>
      <RequestId>E175B041-75A2-4335-B3AC-0FD008F93627</RequestId>
</ListComputeJobLogsResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"E175B041-75A2-4335-B3AC-0FD008F93627",
	"JobLogs":{
		"JobLog":[
			"aaa.log",
			"bbb.log"
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/cityvisual)查看更多错误码。

