### 企业流向闭合告警列表

#### 查询运单二维码 {#-0}

##### 接口地址
```
/app/dyAlarmClosure/listCompanyNumberClose/{pageNum}/{pageSize}
```
##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| pageNum | Integer | 页码 | TRUE |
| pageSize | Integer | 每页记录数 | TRUE |
| transportBeginTime| String | 运输起始时间| FALSE |
| transportEndTime | String | 运输结束时间 | FALSE |
| chemicalId | Long| 危化品ID | FALSE |
| chemicalName | String | 危化品名称 | FALSE |
| transportCompanyName | String  | 运输企业名称| FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| transportCompanyId | String | 运输企业Id|
| transportCompanyName | String | 运输企业名称|
| comfirmdWeightSend | String  |总发货量  |
| comfirmdLoadWeightSend | String | 总装货量 |
| comfirmdWeight | String | 总收货量 |
| comfirmdLoadWeight | String | 总卸货量 |
| sendClose| String | 发货闭合率 |
| transportClose| String |运输闭合率 |
| receiveClose| String  |收货闭合率|
| chemicalUnit| String |单位 |

##### 调用示例
```
url:/app/dyAlarmClosure/listCompanyNumberClose/1/1
```

##### 响应示例
``` json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 3,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 1,
        "pages": 1,
        "list": [
            {
                "transportCompanyId": 990513,
                "transportCompanyName": "中国石油天然气运输公司广东分公司",
                "comfirmdWeightSend": 0,
                "comfirmdLoadWeightSend": 0,
                "comfirmdWeight": 0,
                "comfirmdLoadWeight": 0,
                "sendClose": null,
                "transportClose": null,
                "receiveClose": null,
                "chemicalUnit": null
            }
        ],
        "prePage": 0,
        "nextPage": 0,
        "isFirstPage": true,
        "isLastPage": true,
        "hasPreviousPage": false,
        "hasNextPage": false,
        "navigatePages": 8,
        "navigatepageNums": [
            1
        ],
        "navigateFirstPage": 1,
        "navigateLastPage": 1,
        "lastPage": 1,
        "firstPage": 1
    },
    "message": "成功"
}
```

