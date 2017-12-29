### 企业流向闭合告警详情

#### 查询运单二维码 {#-0}

##### 接口地址

```
/app/dyAlarmClosure/listCompanyNumberCloseBill/{pageNum}/{pageSize}
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
| transportCompanyId | Long | 运输企业ID | TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| billNo | String | 运单号码 |
| transportBeginTime | String | 运单时间 |
| numberPlate | String | 车牌号 |
| transportCompanyName | String | 运输企业名称 |
| chemicalName | String | 危化品名称 |
| sendCompanyName | String | 发货企业名称 |
| receiveCompanyName | String | 收货企业名称 |
| comfirmdWeightSend | String | 发货量 |
| comfirmdLoadWeightSend | String | 装货量 |
| comfirmdWeight | String | 收货量 |
| comfirmdLoadWeight | String | 卸货量 |
| comfirmdTimeSend | String | 发货确认时间 |
| comfirmdTime | String | 收货确认时间 |
| comfirmdLoadTimeSend | String | 装货确认时间 |
| comfirmdLoadTime | String | 卸货确认时间 |
| sendClose | boolean | 发货是否闭合 |
| transportClose | boolean | 运输是否闭合 |
| receiveClose | boolean | 收货是否闭合 |

##### 调用示例

```
url:/app/dyAlarmClosure/listCompanyNumberCloseBill/1/1000?transportCompanyId=990513
```

##### 响应示例

```json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 10,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 1,
        "pages": 1,
        "list": [
            {
                "billNo": "20161212122839001605",
                "transportBeginTime": null,
                "numberPlate": "粤A93590",
                "transportCompanyName": "中国石油天然气运输公司广东分公司",
                "chemicalName": "乙酸烯丙酯",
                "chemicalUnit": null,
                "sendCompanyName": "13",
                "receiveCompanyName": null,
                "comfirmdWeightSend": null,
                "comfirmdLoadWeightSend": null,
                "comfirmdWeight": null,
                "comfirmdLoadWeight": null,
                "comfirmdTimeSend": null,
                "comfirmdTime": null,
                "comfirmdLoadTimeSend": null,
                "comfirmdLoadTime": null,
                "sendClose": true,
                "transportClose": true,
                "receiveClose": true
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



