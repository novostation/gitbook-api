#### 查询常用车辆

##### 接口地址

```
/app/bsVehicleUsing/listPage
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
| numberPlate| String| 车牌号 |FALSE|



##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| vehicleId| Long| 常用车辆iD |
| numberPlate| String | 车牌号 | 
| numberPlateColor| String | 车牌颜色 | 
| vehicleType| String |  车辆类别  | 
| approvedWeight| Float| 核定载重量 | 
| approvedVolume| Float | 核定运输体积|
| transRange| String | 经营范围 | 

##### 调用示例

```
url:/app/bsVehicleUsing/listPage
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
        "total": 24,
        "pages": 24,
        "list": [
            {
                "vehicleId": 20000054,
                "companyId": 20000004,
                "numberPlate": "测试专用5-黄",
                "numberPlateColor": "黄",
                "vehicleType": "",
                "vehicleCategory": "",
                "approvedWeight": 20,
                "approvedVolume": 20,
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
                "transRange": "危险货物运输[3类、4类2项（仅准许运输：活性碳）、5类1项、6类1项（仅准许运输：钡化合物，未另作规定的）、8类、强腐蚀性危险货物] 禁运爆炸品，剧毒化学品。\t",
                "companyNo": "",
                "companyName": "",
                "vehicleCategoryCode": 1,
                "remark": "",
                "createdUser": "",
                "createdUserId": "",
                "createdTime": "2018-01-16 20:40:06"
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

