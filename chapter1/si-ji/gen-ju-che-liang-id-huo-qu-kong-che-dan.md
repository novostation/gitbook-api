#### 获取用户未使用的空车单

##### 接口地址

```
/app/dyBillEmpty/getDyBillEmpty
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| vehicleId| Integer | 车辆ID| FALSE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| emptyId| Integer | 空车单ID|
| billId| Integer | 运单ID|
| billNo| Integer | 运单号|
| vehicleId| Integer | 车辆ID|
| numberPlate| Integer | 车牌|
| tailerVehicleId| Integer | 挂车ID |
| tailerNumberPlate| Integer | 挂车车牌 |
| driverId| Integer |司机ID|
| driverName| String | 司机名称 |
| driverContactNo| String| 司机号码 |
| escortId|Integer | 押运员ID |
| escortName| String| 押运员名称 |
| escortContactNo| String| 押运员号码 |
| createdTime|String| 创建时间 |
| createdUser| String| 创建用户 |
| createdUserId| Integer | 创建用户ID |

##### 调用示例

```
url:/app/dyBillEmpty/getDyBillEmpty

参数:{vehicleId:1415357}
```

##### 响应示例
```
{
    "status": 1,
    "data": {
        "emptyId": 7,
        "billId": 1,
        "billNo": "",
        "vehicleId": 1415357,
        "numberPlate": "粤A64030",
        "tailerVehicleId": 2000847,
        "tailerNumberPlate": "粤AB250挂",
        "driverId": 3,
        "driverName": "陈跃祥",
        "driverContactNo": "89007946",
        "escortId": 1,
        "escortName": "刘佳",
        "escortContactNo": "18922743848",
        "createdTime": "2018-01-16 14:01:34",
        "createdUser": "zhangsan",
        "createdUserId": 1
    },
    "message": "成功"
}
```