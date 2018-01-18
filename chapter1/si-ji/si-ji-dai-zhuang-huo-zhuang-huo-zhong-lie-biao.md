#### 111

##### 接口地址

```
/app/dyBill/driverSearch
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
| loadConfirm| String| 待装货装货中标识| TRUE |
| billNo| String| 运单号| FALSE|
| startTime| String| 开始时间| FALSE |
| endTime| String| 结束时间| FALSE|

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
| billId| Integer | 运单ID|
| billNo| String| 运单号|
| predictUnloadDate| String | 预到日期|
| numberPlate| String| 车牌号 |
| codeName| String| 运单状态 |
| loadStatus| String| 装卸货状态 |

##### 调用示例

```
url:/app/dyBill/driverSearch
参数:{pageNum:1,pageSize:1,loadConfirm:1}
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
        "total": 4,
        "pages": 4,
        "list": [
            {
                "origId": "",
                "billId": 70726,
                "billNo": "20180112749041",
                "vehicleId": 20000054,
                "numberPlate": "测试专用5-黄",
                "numberPlateColor": "黄",
                "tailerVehicleId": 20000045,
                "tailerNumberPlate": "粤C12345-黄",
                "tailerNumberPlateColor": "黄",
                "driverContactNo": "13634564556",
                "escortContactNo": "",
                "driverId": 6909,
                "driverName": "www",
                "driverCertificateNo": "23435345345",
                "escortId": 6831,
                "escortName": "777",
                "escortCertificateNo": "",
                "transportCompanyId": 20000004,
                "transportCompanyNo": "",
                "transportCompanyName": "广州中石化",
                "loadGoodsDate": "2018-01-12 00:00:00",
                "unloadGoodsDate": "",
                "predictUnloadDate": "2018-01-13 00:00:00",
                "transportBeginTime": "2018-01-12 16:53:56",
                "transportEndTime": "",
                "createdTime": "2018-01-12 16:53:26",
                "createdUser": "zhangsan",
                "createdUserId": 1,
                "updatedTime": "2018-01-12 16:53:56",
                "updatedUser": "zhangsan",
                "billStatus": 1,
                "billSource": 2,
                "remark": "",
                "endFlag": "",
                "endApp": "",
                "weight": "",
                "chemicalName": "",
                "codeName": "待装货",
                "loadStatus": "待装货",
                "permitWeight": "",
                "vehicleSpec": "",
                "vehicleVendor": "",
                "vehicleCatogery": ""
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
            4
        ],
        "navigateFirstPage": 1,
        "navigateLastPage": 4,
        "firstPage": 1,
        "lastPage": 4
    },
    "message": "成功"
}
```
