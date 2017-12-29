#### 获取运单完整信息

##### 接口地址
```
/app/dyBill/getInfoById/{billNo}
```
##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo| String| 运单号 | TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |
| billId | Number | 运单id |  |
| origId | String | orig_id |
| billNo | String | 运单号 |
| vehicleId | Number | 车辆id |
| numberPlate | String | 运输车牌号 | 
| numberPlateColor | String | 运输车辆车牌颜色 |
| tailerVehicleId | String | 挂车车牌颜色 | 
| tailerNumberPlate | Number | 挂车车辆id | 
| tailerNumberPlateColor | String | 挂车车牌号 | 
| driverId | Number | 驾驶员id(从业人员id) | 
| driverName | String | 驾驶员 |
| driverCertificateNo | String | 驾驶员资格证号 | 
| escortContactNo | String | 驾驶员联系电话 | 
| escortId | Number | 押运员id | 
| escortName | String | 押运员名称 | 
| escortCertificateNo | String | 押运员资格证号 | 
| escortContactNo | String | 押运员联系电话 | 
| transportCompanyId | Number | 运输公司id | 
| transportCompanyNo | String | 运输企业社会编号 | 
| transportCompanyName | String | 运输企业名称 | 
| loadGoodsDate | String | 装货日期 | 
| unloadGoodsDate | String | 卸货日期 | 
| predictUnloadDate | String | 预到日期 | 
| transportBeginTime | String | 运单开始时间 | 
| transportEndTime | String | 运单结束时间 | 
| createdTime | String | 运单创建时间 | 
| createdUser | String | 创建人员 | 
| updatedTime | String | 更新时间 | 
| updatedUser | String | 更新人员 | 
| billStatus | Number | 运单状态 1 ：待装货 2：装货中 3 ：运输中 4：已卸货 5 ：已完成 6:已取消 | 
| billSource | Number | 1: 来源于运单系统\n2：来源于手机app | 
| remark | String | remark | 


##### 调用示例
```
url:/app/dyBill/getInfoById/14483
```
参数:

##### 响应示例
``` json
{
    "status": 1,
    "data": {
        "origId": "0Z8958Z1N6FV",
        "billId": 14483,
        "billNo": "20171111279076",
        "vehicleId": 2614874,
        "numberPlate": "粤AH6088-黄",
        "numberPlateColor": "黄",
        "tailerVehicleId": null,
        "tailerNumberPlate": null,
        "tailerNumberPlateColor": null,
        "driverContactNo": "88131363",
        "escortContactNo": "88131363",
        "driverId": 576,
        "driverName": "高国玉",
        "driverCertificateNo": "412925197211123278",
        "escortId": 2491,
        "escortName": "严伟国",
        "escortCertificateNo": "440111196302050112",
        "transportCompanyId": 4,
        "transportCompanyNo": "A1000005",
        "transportCompanyName": "广州二运集团有限公司",
        "loadGoodsDate": "2017-11-12 00:00:00",
        "unloadGoodsDate": null,
        "predictUnloadDate": "2017-11-12 00:00:00",
        "transportBeginTime": null,
        "transportEndTime": null,
        "createdTime": "2017-11-11 16:58:21",
        "createdUser": "广州二运集团有限公司",
        "updatedTime": "2017-11-14 14:40:23",
        "updatedUser": null,
        "billStatus": 4,
        "billSource": 1,
        "remark": "接口同步数据",
        "weight": 7.5,
        "chemicalName": "瓦斯油或柴油或轻质燃料油,瓦斯油或柴油或轻质燃料油",
        "codeName": "已卸货",
        "loadStatus": "卸货完毕",
        "permitWeight": null,
        "vehicleSpec": null,
        "vehicleVendor": null,
        "vehicleCatogery": null,
        "dyBillShipReceiveUnitDtoList1": [
            {
                "origId": "0Z8958Z1N6GH",
                "billUnitId": 24726,
                "billId": 14483,
                "billNo": "20171111279076",
                "companyId": 4,
                "bsUnitId": null,
                "unitName": "广州二运集团有限公司茅岗加油站",
                "unitType": 1,
                "contactPerson": "杨文乾",
                "contactTel": "13829157610",
                "fax": null,
                "remark": "接口同步数据",
                "createdUser": null,
                "dyBillAddressDtoList": [
                    {
                        "billAddressId": 41154,
                        "origId": "0Z8958Z1N6GH0Z8958Z1N6GK",
                        "bsAddressId": null,
                        "billUnitId": 24726,
                        "billId": 14483,
                        "provinceId": "40",
                        "provinceName": "广东",
                        "cityId": "39",
                        "cityName": "广州",
                        "regionId": "32",
                        "regionName": "黄埔",
                        "roadDetail": "广东省 广州市 市辖区 黄埔大道",
                        "addressType": "1",
                        "addressName": "广东省 广州市 市辖区 黄埔大道",
                        "chemicalUnit": "吨",
                        "totalWeight": 7.5,
                        "totalVolume": 0,
                        "loadCkeckUserId": 576,
                        "loadCheckUserName": "高国玉",
                        "loacCheckUserTel": "88131363",
                        "loadCheckTime": "2017-11-12 05:44:47",
                        "loadCheckTotalWeight": 7.5,
                        "loadCheckTotalVolume": 0,
                        "loadCheckRemark": "",
                        "ckeckUserId": null,
                        "ckeckUserName": null,
                        "checkUserTel": null,
                        "ckeckCompanyId": null,
                        "ckeckCompanyName": null,
                        "ckeckTime": null,
                        "ckeckTotalWeight": null,
                        "ckeckTotalVolume": null,
                        "ckeckRemark": null,
                        "transType": 1,
                        "dyBillChemicalDtoList": [
                            {
                                "id": 44100,
                                "origId": "A0Z8958Z1N6GG0YKRG7F00RFZⅢ",
                                "billId": 14483,
                                "billAddressId": 41154,
                                "billUnitId": 24726,
                                "chemicalId": 944,
                                "chemicalName": "瓦斯油或柴油或轻质燃料油",
                                "chemicalType": 3,
                                "chemicalItemNo": null,
                                "chemicalUnit": "吨",
                                "packLevel": 3,
                                "unionCode": "1202",
                                "weight": 7.5,
                                "volume": 0,
                                "driveMileage": null,
                                "checkWeight": null,
                                "checkVolume": null,
                                "loadCheckWeight": null,
                                "loadCheckVolume": null,
                                "transType": 1,
                                "chemicalTypeName": null,
                                "chemicalAlias": null
                            }
                        ]
                    }
                ]
            }
        ],
        "dyBillShipReceiveUnitDtoList2": [
            {
                "origId": "0Z8958Z1N6GJ",
                "billUnitId": 24727,
                "billId": 14483,
                "billNo": "20171111279076",
                "companyId": 4,
                "bsUnitId": null,
                "unitName": "广州二运集团有限公司茅岗加油站",
                "unitType": 2,
                "contactPerson": "赵东生",
                "contactTel": "13710862511",
                "fax": null,
                "remark": "接口同步数据",
                "createdUser": null,
                "dyBillAddressDtoList": [
                    {
                        "billAddressId": 41155,
                        "origId": "0Z8958Z1N6GJ0Z8958Z1N6GL",
                        "bsAddressId": null,
                        "billUnitId": 24727,
                        "billId": 14483,
                        "provinceId": "40",
                        "provinceName": "广东",
                        "cityId": "39",
                        "cityName": "广州",
                        "regionId": "32",
                        "regionName": "黄埔",
                        "roadDetail": "广东省 广州市 黄埔区 茅岗380号",
                        "addressType": "2",
                        "addressName": "广东省 广州市 黄埔区 茅岗380号",
                        "chemicalUnit": "吨",
                        "totalWeight": 0,
                        "totalVolume": 0,
                        "loadCkeckUserId": 576,
                        "loadCheckUserName": "高国玉",
                        "loacCheckUserTel": "88131363",
                        "loadCheckTime": "2017-11-12 05:44:53",
                        "loadCheckTotalWeight": 7.5,
                        "loadCheckTotalVolume": 0,
                        "loadCheckRemark": "",
                        "ckeckUserId": null,
                        "ckeckUserName": null,
                        "checkUserTel": null,
                        "ckeckCompanyId": null,
                        "ckeckCompanyName": null,
                        "ckeckTime": null,
                        "ckeckTotalWeight": null,
                        "ckeckTotalVolume": null,
                        "ckeckRemark": null,
                        "transType": 2,
                        "dyBillChemicalDtoList": [
                            {
                                "id": 44101,
                                "origId": "0Z8958Z1N6GG0YKRG7F00RFZAⅢ",
                                "billId": 14483,
                                "billAddressId": 41155,
                                "billUnitId": 24727,
                                "chemicalId": 944,
                                "chemicalName": "瓦斯油或柴油或轻质燃料油",
                                "chemicalType": 3,
                                "chemicalItemNo": null,
                                "chemicalUnit": "吨",
                                "packLevel": 3,
                                "unionCode": "1202",
                                "weight": 0,
                                "volume": 0,
                                "driveMileage": null,
                                "checkWeight": null,
                                "checkVolume": null,
                                "loadCheckWeight": null,
                                "loadCheckVolume": null,
                                "transType": 2,
                                "chemicalTypeName": null,
                                "chemicalAlias": null
                            }
                        ]
                    }
                ]
            }
        ]
    },
    "message": "获取数据成功"
}
```
