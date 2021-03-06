# ListResourcePool {#concept_ow4_s1s_2gb .concept}

调用 ListResourcePool 接口查询资源池列表

## 请求参数 {#section_obj_yxl_2gb .section}

|参数|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|ClusterId|String|是|C-EBD62A703A430E23|集群 ID|
|RegionId|String|是|cn-hangzhou|区域 ID|
|PoolType|String|否|CAPACITY\_SCHEDULER|资源池类型，合法值：CAPACITY\_SCHEDULER,FAIR\_SCHEDULER|
|AccessKeyId|String|是|LTAI8ljWyu7y\*\*\*\*|阿里云 AccessKey ID 信息|

## 返回参数 {#section_vbj_yxl_2gb .section}

|字段|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|A544317F-4A60-4532-AC96-191B9D80420A|请求 ID|
|PageNumber|Integer|1|当前的页号|
|PageSize|Integer|100|每页的记录数|
|Total|Integer|10|总记录数|
|PoolInfoList| | |资源池列表|
|QueueList| | |资源池队列列表|
|EcmResourcePoolConfigList| | |资源池配置|
|Id|Long|2926|参数 ID|
|ConfigKey|String|minimum-user-limit-percent|参数 Key|
|ConfigValue|String|0|参数值|
|ConfigType|String|RESOURCE\_QUEUE\_CONFIG|参数类型|
|Category|String|QUEUE\_RESOURCE\_LIMIT|参数类别|
|Status|String|NORMAL|参数状态|
|Note|String|test|参数描述|
|EcmResourceQueue| | |资源队列|
|Id|Long|2928|队列 ID|
|Name|String|DEFAULT2|队列名称|
|QualifiedName|String|default|QualifiedName|
|QueueType|String|null|队列类型|
|ParentQueueId|Long|116|父队列 ID|
|Leaf|Boolean|false|是否叶子节点|
|Status|String|NORMAL|队列状态|
|UserId|String|15283423567645362|用户 ID|
|ResourcePoolId|Long|116|资源池 ID|
|EcmResourcePoolConfigList| | |资源池配置列表|
|Id|Long|2926|参数 ID|
|ConfigKey|String|minimum-user-limit-percent|参数 Key|
|ConfigValue|String|0|参数值|
|ConfigType|String|RESOURCE\_QUEUE\_CONFIG|参数类型|
|Category|String|QUEUE\_RESOURCE\_LIMIT|参数类别|
|Status|String|NORMAL|参数状态|
|Note|String|test|参数描述|
|EcmResourcePool| | |资源池|
|Id|Long|116|资源池 ID|
|Name|String|DEFAULT|资源池名称|
|PoolType|String|CAPACITY\_SCHEDULER|资源池类型|
|Active|Boolean|true|激活状态|
|Note|String|test|资源池描述|
|UserId|String|15283423567645362|用户 ID|
|YarnSiteConfig|String|null|YarnSite 配置|

## 示例 {#section_dcj_yxl_2gb .section}

-   请求示例

    ```
    /?ClusterId=C-EBD62A703A430E23
    &RegionId=cn-hangzhou
    &AccessKeyId=LTAI8ljWyu7y****
    &PoolType=CAPACITY_SCHEDULER
    &<公共请求参数>
    ```

-   正常返回示例

    JSON 格式

    ```
    {
    	"code":"200",
    	"data":{
    		"PoolInfoList":{
    			"PoolInfo":[
    				{
    					"EcmResourcePool":{
    						"Active":true,
    						"Id":116,
    						"Name":"DEFAULT",
    						"Note":"",
    						"PoolType":"CAPACITY_SCHEDULER",
    						"UserId":"1528342317645362",
    						"YarnSiteConfig":""
    					},
    					"EcmResourcePoolConfigList":{
    						"EcmResourcePoolConfig":[]
    					},
    					"QueueList":{
    						"Queue":[{
    							"EcmResourcePoolConfigList":{
    								"EcmResourcePoolConfig":[
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"capacity",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"100",
    										"Id":2925,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"minimum-user-limit-percent",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"0",
    										"Id":2926,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"maximum-capacity",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"0",
    										"Id":2927,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"user-limit-factor",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2928,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"maximum-allocation-mb",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2929,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"maximum-allocation-vcores",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2930,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"maximum-applications",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2931,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"maximum-am-resource-percent",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2932,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_RESOURCE_LIMIT",
    										"ConfigKey":"state",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"RUNNING",
    										"Id":2933,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_SUBMISSION_ACCESS_CONTROL",
    										"ConfigKey":"acl_submit_applications",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2934,
    										"Note":"",
    										"Status":"NORMAL"
    									},
    									{
    										"Category":"QUEUE_ADMINISTRATION_ACCESS_CONTROL",
    										"ConfigKey":"acl_administer_queue",
    										"ConfigType":"RESOURCE_QUEUE_CONFIG",
    										"ConfigValue":"",
    										"Id":2935,
    										"Note":"",
    										"Status":"NORMAL"
    									}
    								]
    							},
    							"EcmResourceQueue":{
    								"Id":247,
    								"Leaf":false,
    								"Name":"default",
    								"ParentQueueId":0,
    								"QualifiedName":"default",
    								"QueueType":"",
    								"ResourcePoolId":116,
    								"Status":"NORMAL",
    								"UserId":"1528342317645362"
    							}
    						}]
    					}
    				},
    				{
    					"EcmResourcePool":{
    						"Active":true,
    						"Id":117,
    						"Name":"pool1",
    						"Note":"",
    						"PoolType":"CAPACITY_SCHEDULER",
    						"UserId":"1528342317645362",
    						"YarnSiteConfig":""
    					},
    					"EcmResourcePoolConfigList":{
    						"EcmResourcePoolConfig":[]
    					},
    					"QueueList":{
    						"Queue":[]
    					}
    				}
    			]
    		},
    		"RequestId":"213DD361-EF38-4A31-A909-96857AEE42DE"
    	},
    	"requestId":"213DD361-EF38-4A31-A909-96857AEE42DE",
    	"successResponse":true
    }
    ```

-   异常返回示例

    JSON 格式

    ```
    {
    	"code":"User.OtherUserResource.NotAllow",
    	"message":"It is not allowed to operate other user's resource",
    	"requestId":"A544317F-4A60-4532-AC96-191B9D80420AF",
    	"successResponse":false
    }
    ```


## 错误码 {#section_fcj_yxl_2gb .section}

[查看本产品错误码](https://error-center.alibabacloud.com/status/product/Emr)

