#### 查询二维码扫码的信息

##### 接口地址

```
/app/querybillNo
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo | String | 运单号 | TRUE|
| billUnitId | Long | 运单收发货方id | TRUE|
| addressId | Long | 运单收发地址id | TRUE|
| addressType| Integer | 1: 发货、装货 2：收货、卸货 | TRUE|

##### 响应参数

格式：JSON
运单信息

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |
| addressType| Integer | 1: 发货、装货 2：收货、卸货 |
| transportCompanyId| Long | 运输企业ID |
| transportCompanyName | String | 运输公司名称 |
| driverName | String | 驾驶员姓名 |
| driverContactNo | String  | 驾驶员电话 |
| escortName | String | 押运员姓名|
| escortContactNo | String | 押运员电话 |
| shipReceiveUnit| JSON| 收发货方信息 |
| billUnitId | Long | 收货企业ID |
| unitName | String | 收发货方名称 |
| name | String | 收货人姓名 |
| phone| String | 收货人电话 |

确认装卸货公司信息

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| checkCompanyChemical| JSON| 确认装卸货公司信息|
|billUnitId | Long | 收货企业ID |
| unitName | String | 收发货方名称 |
| name | String | 收货人姓名 |
| phone| String | 收货人电话 |
| addressName| String | 地址名称 |
| roadDetail| String | 地址详情 |
| addressName| String | 地址名称 |
| list| JSON| 货物 |
| id| Long | 货物id|
| loadCheckWeight| Float| 司机确认重量 |
| loadCheckVolume| Float| 司机确认体积 |
| chemicalId| Long | 化学品id |
| unionCode| String | 化学品国际编号 |
| chemicalUnit| String | 化学品单位 |

##### 调用示例

```
url:/app/querybillNo?billNo=20170511029348&billUnitId=4094&addressType=1&addressId=4017
```

##### 响应示例
```
{
    "status": 1,
    "data": {
        "transportCompanyId": 1767771,
        "checkCompanyChemical": {
            "phone": "4008976866",
            "unitName": "广州广钢气体有限公司",
            "name": "陈嘉亮",
            "billUnitId": 4094,
            "list": [
                {
                    "id": 6267,
                    "chemicalName": "氧[液化的]",
                    "loadCheckWeight": "",
                    "loadCheckVolume": "",
                    "chemicalId": 829,
                    "unionCode": "1073",
                    "chemicalUnit": "吨"
                }
            ],
            "roadDetail": "广州 南沙 红钢路5号",
            "addressName": "广州 南沙 红钢路5号"
        },
        "escortContactNo": "18818867314",
        "shipReceiveUnit": [
            {
                "phone": "4008976866",
                "unitName": "广州广钢气体有限公司",
                "name": "陈嘉亮",
                "billUnitId": 4094
            }
        ],
        "transportCompanyName": "广州广钢气体有限公司",
        "addressType": 1,
        "driverName": "周美胜",
        "escortName": "王天顺",
        "driverContactNo": "13602276573"
    },
    "message": "获取数据成功"
}
```


