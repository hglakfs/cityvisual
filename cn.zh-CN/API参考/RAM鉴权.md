# RAM鉴权 {#concept_1216494 .concept}

在使用RAM账号调用城市视觉智能引擎API之前，需要主账号通过创建授权策略对RAM账号进行授权。在授权策略中，使用资源描述符（Alibaba Cloud Resource Name, ARN）指定授权资源。

## 自定义策略 {#section_uuy_m3i_udn .section}

您可以通过RAM控制台或者调用RAM API [CreatePolicy](https://help.aliyun.com/document_detail/28716.html?spm=a2c4g.11186623.2.12.17235399P7eQcZ#doc-api-977717)创建一个自定义策略，在脚本配置方式的自定义策略中，您需要根据JSON模板文件填写策略内容。其中的Action和Resource参数取值取自本文可授权的城市视觉智能引擎接口的表格中。更多详情请参见[账号访问控制](https://help.aliyun.com/document_detail/25481.html?spm=a2c4g.11186623.2.13.17235399P7eQcZ#concept-stg-4pd-zdb)和[权限策略基本元素](https://help.aliyun.com/document_detail/93738.html?spm=a2c4g.11186623.2.14.17235399P7eQcZ#concept-xg5-51g-xdb)。

``` {#codeblock_kkr_zeb_s60}
{
    "Version": "1",
    "Statement": [
        {
            "Action": [
                "cityvisual:DescribeInstances"
            ],
            "Resource": [
                "acs:cityvisual:$regionid:135696343788****:instance/cityvisual-*****"
            ],
            "Effect": "Allow"
        }
    ]
}
```

## 可授权的城市视觉智能引擎接口 {#section_9il_e6z_5t6 .section}

下表列举了城市视觉智能引擎中可授权的API及其描述方式：

|API|资源描述|
|---|----|
|AttachStream|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid acs:cityvisual:$regionid:$accountid:camera/$cameraid

 |
|BatchModifyCameraStatus|acs:cityvisual:$regionid:$accountid:camera/$cameraid|
|CreateInstance|acs:cityvisual:$regionid:$accountid:instance/\*|
|CreateAlgoLib|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:algolib/\*

 |
|CreateCapability|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:capability/\*

 |
|CreateResourceProfile|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:resourceprofile/\*

 |
|CreateJobGroup|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:jobgroup/\*

 acs:cityvisual:$regionid:$accountid:resourceprofile/$resourceprofileid

 acs:cityvisual:$regionid:$accountid:algolib/$algolibid|
|CreateCamera|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:camera/\*

 |
|CreateWorkGroup|acs:cityvisual:$regionid:$accountid:instance/$instanceid acs:cityvisual:$regionid:$accountid:workgroup/\*

 |
|DescribeInstances|acs:cityvisual:$regionid:$accountid:instance/\* acs:cityvisual:$regionid:$accountid:instance/$instanceid

 |
|DeleteInstance|acs:cityvisual:$regionid:$accountid:instance/$instanceid|
|DescribeAlgoLibs|acs:cityvisual:$regionid:$accountid:algolib/\* acs:cityvisual:$regionid:$accountid:algolib/$algolibid

 |
|DeleteAlgoLib|acs:cityvisual:$regionid:$accountid:algolib/$algolibid|
|DescribeCapabilities|acs:cityvisual:$regionid:$accountid:capability/\* acs:cityvisual:$regionid:$accountid:capability/$capabilityid

 |
|DeleteCapability|acs:cityvisual:$regionid:$accountid:capability/$capabilityid|
|DescribeResourceProfiles|acs:cityvisual:$regionid:$accountid:resourceprofile/\* acs:cityvisual:$regionid:$accountid:resourceprofile/$resourceprofileid

 |
|DeleteResourceProfile|acs:cityvisual:$regionid:$accountid:resourceprofile/$resourceprofileid|
|DescribeJobGroups|acs:cityvisual:$regionid:$accountid:jobgroup/\* acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid

 |
|DeleteJobGroup|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid|
|DescribeStreams|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid acs:cityvisual:$regionid:$accountid:camera/\*

 |
|DetachStream|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid acs:cityvisual:$regionid:$accountid:camera/$cameraid

 |
|DescribeCameras|acs:cityvisual:$regionid:$accountid:camera/\* acs:cityvisual:$regionid:$accountid:camera/$cameraid

 |
|DeleteCamera|acs:cityvisual:$regionid:$accountid:camera/$cameraid|
|DescribeWorkGroups|acs:cityvisual:$regionid:$accountid:workgroup/\* acs:cityvisual:$regionid:$accountid:workgroup/$workgroupid

 |
|DeleteWorkGroup|acs:cityvisual:$regionid:$accountid:workgroup/$workgroupid|
|DescribeProtocols|acs:cityvisual:$regionid:$accountid:workgroup/$workgroupid|
|GetComputeJobLog|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid|
|GetStreamsForCameras|acs:cityvisual:$regionid:$accountid:camera/$cameraid|
|ListComputeJobLogs|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid|
|ModifyInstance|acs:cityvisual:$regionid:$accountid:instance/$instanceid|
|ModifyAlgoLib|acs:cityvisual:$regionid:$accountid:algolib/$algolibid|
|ModifyCapability|acs:cityvisual:$regionid:$accountid:capability/$capabilityid|
|ModifyResourceProfile|acs:cityvisual:$regionid:$accountid:resourceprofile/$resourceprofileid|
|ModifyJobGroup|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid acs:cityvisual:$regionid:$accountid:resourceprofile/$resourceprofileid

 acs:cityvisual:$regionid:$accountid:algolib/$algolibid

 |
|ModifyCamera|acs:cityvisual:$regionid:$accountid:camera/$cameraid|
|ModifyWorkGroup|acs:cityvisual:$regionid:$accountid:workgroup/$workgroupid|
|SearchImages|acs:cityvisual:$regionid:$accountid:\*|
|StartJobGroup|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid|
|StopJobGroup|acs:cityvisual:$regionid:$accountid:jobgroup/$jobgroupid|

