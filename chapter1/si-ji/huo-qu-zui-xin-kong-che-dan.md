#### 获取最新空车单

##### 接口地址

```
/app/dyBillEmpty/getLatestDyBillEmpty
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

 格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
|vehicleId| Long| 车辆ID | FALSE|



##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：存在空车单；0：没有空车单 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| emptyId| Long| 空车单iD |
| billId| Long| 运单iD |
| billNo| Long| 运单号 |
| vehicleId| Long| 车辆iD |
| numberPlate| String | 车牌号 | 

存在运单id就说明是未使用的空车单

##### 调用示例

```
url:/app/dyBillEmpty/getLatestDyBillEmpty
```

##### 响应示例
```
{
    "status": 1,
    "data": {
        "emptyId": 8,
        "billId": "",
        "billNo": "",
        "vehicleId": 1415357,
        "numberPlate": "粤A64030-黑",
        "tailerVehicleId": 2000847,
        "tailerNumberPlate": "粤AB250挂-黄",
        "driverId": 3,
        "driverName": "陈跃祥",
        "driverContactNo": "89007946",
        "escortId": 1,
        "escortName": "刘佳",
        "escortContactNo": "18922743848",
        "createdTime": "2018-01-17 11:35:06",
        "createdUser": "zhangsan",
        "createdUserId": 1,
        "endTime": ""
    },
    "message": "用户找到1条未使用的空车单"
}
```