#### 司机待确认装货列表

##### 接口地址

```
/app/confirm/driverLoadConfirmList
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| pageNum| Integer | 页码| TRUE |
| pageSize| Integer | 每页最大数量| TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| pageNum| Integer | 页码|
| pageSize| Integer | 每页最大数量|
| list| JSON数组| 响应数据|
| billNo| String| 运单号 |
| unitName| String | 收发货方|
| loadCheckTime| String| 司机确认时间 |
| ckeckTime| String| 企业确认时间 |
| dyBillAddressChemicalDtoList| JSON数组| 货物信息 |
| chemicalName| String| 货物名称 |
| chemicalUnit| String| 货物单位 |
| checkWeight| String| 企业确认重量 |
| checkVolume| String| 企业确认体积 |
| loadCheckWeight| String| 司机确认重量 |
| loadCheckVolume| String| 司机确认体积 |

##### 调用示例

```
url:/app/confirm/driverLoadConfirmList

参数:{pageNum:1,pageSize:1}
```

##### 响应示例
``` json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 1,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 34,
        "pages": 34,
        "list": [
            {
                "billNo": "20171124313090",
                "unitName": "揭阳市忠泰气体厂有限公司普宁市南溪镇后寨村狮尾山",
                "loadCheckTime": "0001-01-01 00:00:00",
                "ckeckTime": "",
                "dyBillAddressChemicalDtoList": [
                    {
                        "chemicalName": "氧[液化的]",
                        "chemicalUnit": "吨",
                        "checkWeight": "",
                        "checkVolume": "",
                        "loadCheckWeight": "",
                        "loadCheckVolume": ""
                    }
                ]
            }
        ],
        "prePage": 0,
        "nextPage": 2,
        "isFirstPage": true,
        "isLastPage": false,
        "hasPreviousPage": false,
        "hasNextPage": true,
        "navigatePages": 8,
        "navigatepageNums": [
            1,
            2,
            3,
            4,
            5,
            6,
            7,
            8
        ],
        "navigateFirstPage": 1,
        "navigateLastPage": 8,
        "firstPage": 1,
        "lastPage": 8
    },
    "message": "成功"
}
```
