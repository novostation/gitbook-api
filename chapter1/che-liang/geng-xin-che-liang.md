#### 更新车辆

##### 接口地址

```
/app/bsVehicle/update
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| vehicleId| Long| 车辆iD |TRUE|
| numberPlate| String | 车牌号 | TRUE|
| numberPlateColor| String | 车牌颜色 | TRUE|
| vehicleType| String |  车辆类别  | TRUE|
| approvedWeight| Float| 核定载重量 | FALSE |
| approvedVolume| Float | 核定运输体积| FALSE |
| transRange| String | 经营范围 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| vehicleId| Long| 车辆iD |
##### 调用示例

```
url:/app/bsVehicle/update


参数:

{
        "vehicleId": 20000055,
        "numberPlate": "321",
        "numberPlateColor": "231",
        "vehicleType": "1",
        "vehicleCategory": "",
        "approvedWeight": 132,
        "approvedVolume": 312,
        "transRange": "31"
}
```



##### 响应示例

```
{
    "status": 1,
    "data": 20000055,
    "message": "更新数据成功"
}
```

