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
| billNo| String| 运单号 | FALSE|

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
| id| Long| 货物主键ID |
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
        "pageSize": 10,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 2,
        "pages": 1,
        "list": [
            {
                "billNo": "20180120293032",
                "unitName": "广东胜捷消防科技有限公司",
                "loadCheckTime": "",
                "ckeckTime": "",
                "dyBillAddressChemicalDtoList": [
                    {
                        "id": 36600,
                        "chemicalName": "别名1",
                        "chemicalUnit": "吨",
                        "checkWeight": 5,
                        "checkVolume": "",
                        "loadCheckWeight": "",
                        "loadCheckVolume": ""
                    },
                    {
                        "id": 36601,
                        "chemicalName": "别名2",
                        "chemicalUnit": "吨",
                        "checkWeight": 5,
                        "checkVolume": "",
                        "loadCheckWeight": "",
                        "loadCheckVolume": ""
                    }
                ]
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
        "firstPage": 1,
        "lastPage": 1
    },
    "message": "成功"
}
```
