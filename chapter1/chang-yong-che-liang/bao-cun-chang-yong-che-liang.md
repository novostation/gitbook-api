#### 保存常用车辆

##### 接口地址

```
/app/bsVehicleUsing/save
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| numberPlate| String | 车牌号 | TRUE|
| numberPlateColor| String | 车牌颜色 | TRUE|
| vehicleType| String |  车辆类别  | TRUE|
| approvedWeight| Float| 核定载重量 | FALSE |
| approvedVolume| Float | 核定运输体积| FALSE |
| vehicleCategoryCode| Integer | 1:货车  2：牵引车 ：3 : 挂车 |TRUE|
| transRange| String | 经营范围 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| vehicleId| Long| 常用车辆ID |
##### 调用示例

```
url:/app/bsVehicleUsing/save

参数:

{       
        "numberPlate": "321",
        "numberPlateColor": "231",
        "vehicleType": "1",
        "vehicleCategory": "",
        "approvedWeight": 132,
        "approvedVolume": 312,   
        "vehicleCategoryCode":1,    
        "transRange": "31"       
}
```



##### 响应示例

```
{
    "status": 1,
    "data": 6970,
    "message": "保存数据成功"
}
```

