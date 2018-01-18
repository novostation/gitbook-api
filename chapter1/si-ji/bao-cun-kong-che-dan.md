#### 保存空车单

##### 接口地址

```
/app/dyBillEmpty/save
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| vehicleId| Integer | 车辆ID| TRUE |
| tailerVehicleId| Integer | 挂车ID |FALSE|
| driverId| Integer |司机ID|TRUE |
| driverName| String | 司机名称 |TRUE |
| driverContactNo| String| 司机号码 |TRUE |
| escortId|Integer | 押运员ID |TRUE |
| escortName| String| 押运员名称 |TRUE |
| escortContactNo| String| 押运员号码 |TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| emptyId| Integer | 空车单ID|

##### 调用示例

```
url:/app/dyBillEmpty/save

参数:
{
"vehicleId": 1415357,
"tailerVehicleId": 2000847,
"driverId": 3,
"driverName": "陈跃祥",
"driverContactNo": "89007946",
"escortId": 1,
"escortName": "刘佳",
"escortContactNo": "18922743848",
}
```

##### 响应示例
```
{
    "status": 1,
    "data": 7,
    "message": "保存数据成功"
}
```