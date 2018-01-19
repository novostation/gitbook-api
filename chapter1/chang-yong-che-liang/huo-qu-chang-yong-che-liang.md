#### 获取车辆

##### 接口地址

```
/app/bsVehicleUsing/getInfoById/{vehicleId}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
|vehicleId| Long| 常用车辆ID | TRUE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| vehicleId| Long| 车辆iD |
| numberPlate| String | 车牌号 | 
| numberPlateColor| String | 车牌颜色 | 
| vehicleType| String |  车辆类别  | 
| approvedWeight| Float| 核定载重量 | 
| approvedVolume| Float | 核定运输体积|
| transRange| String | 经营范围 | 


##### 调用示例

```
url:/app/bsVehicleUsing/getInfoById/20000055
```

##### 响应示例

``` json
{
    "status": 1,
    "data": {
        "vehicleId": 20000055,
        "companyId": 1767771,
        "numberPlate": "321",
        "numberPlateColor": "231",
        "vehicleType": "1",
        "vehicleCategory": "",
        "approvedWeight": 132,
        "approvedVolume": 312,
        "vendor": "",
        "model": "",
        "fuelType": "",
        "engineModel": "",
        "transportCertificateWord": "",
        "transportCertificateNo": "",
        "certificateExpireDate": "",
        "auditExpireDate": "",
        "auditResult": "",
        "length": "",
        "width": "",
        "height": "",
        "equipmentLevel": "",
        "firstTransportDate": "",
        "buyDate": "",
        "uselessDate": "",
        "isEquipGps": "",
        "isImport": "",
        "totalWeight": "",
        "drivingLicense": "",
        "potVolume": "",
        "potSize": "",
        "exhaustSize": "",
        "transRange": "31",
        "companyNo": "",
        "companyName": "",
        "vehicleCategoryCode": "",
        "remark": "",
        "createdUser": "zhangsan",
        "createdUserId": 1,
        "createdTime": "2018-01-16 20:27:19"
    },
    "message": "获取数据成功"
}
```

