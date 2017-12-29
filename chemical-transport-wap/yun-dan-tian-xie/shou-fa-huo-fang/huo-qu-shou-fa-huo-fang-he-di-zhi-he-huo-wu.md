#### 获取收发货方货物

##### 接口地址

```
/app/dyBillShipReceiveUnit/getInfoById/14483/{billId}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billId| String | 运单号 | Y |
| transType| Integer | 1:发货方；2:收货方 | N |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
/app/dyBillShipReceiveUnit/getInfoById/14483
```

参数

```
{transType：1}
```

响应示例

``` json
{
    "unitType": null,
    "shipAdderssGoodsMes": [
        {
            "addressMes": {
                "billAddressId": 22524,
                "origId": "0Z6U1V51C3GW0Z6U1V51C3H0",
                "bsAddressId": null,
                "billUnitId": 14483,
                "billId": 9409,
                "provinceId": "40",
                "provinceName": "广东",
                "cityId": "39",
                "cityName": "广州",
                "regionId": "29",
                "regionName": "天河",
                "roadDetail": "广东省 广州市 天河区 广州珠村",
                "addressType": "2",
                "addressName": "广东省 广州市 天河区 广州珠村",
                "chemicalUnit": null,
                "totalWeight": 0,
                "totalVolume": 0,
                "loadCkeckUserId": 326,
                "loadCheckUserName": null,
                "loacCheckUserTel": null,
                "loadCheckTime": null,
                "loadCheckTotalWeight": null,
                "loadCheckTotalVolume": null,
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
                "transType": 2
            },
            "addressGoodsMes": [
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23967,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22524,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23966,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22523,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23965,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22522,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                }
            ]
        },
        {
            "addressMes": {
                "billAddressId": 22523,
                "origId": "0Z6U1V51C3GW0Z6U1V51C3GZ",
                "bsAddressId": null,
                "billUnitId": 14483,
                "billId": 9409,
                "provinceId": "40",
                "provinceName": "广东",
                "cityId": "39",
                "cityName": "广州",
                "regionId": "29",
                "regionName": "天河",
                "roadDetail": "广东省 广州市 天河区 广州珠村",
                "addressType": "2",
                "addressName": "广东省 广州市 天河区 广州珠村",
                "chemicalUnit": null,
                "totalWeight": 0,
                "totalVolume": 0,
                "loadCkeckUserId": 326,
                "loadCheckUserName": null,
                "loacCheckUserTel": null,
                "loadCheckTime": null,
                "loadCheckTotalWeight": null,
                "loadCheckTotalVolume": null,
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
                "transType": 2
            },
            "addressGoodsMes": [
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23967,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22524,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23966,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22523,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23965,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22522,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                }
            ]
        },
        {
            "addressMes": {
                "billAddressId": 22522,
                "origId": "0Z6U1V51C3GW0Z6U1V51C3GY",
                "bsAddressId": null,
                "billUnitId": 14483,
                "billId": 9409,
                "provinceId": "40",
                "provinceName": "广东",
                "cityId": "39",
                "cityName": "广州",
                "regionId": "29",
                "regionName": "天河",
                "roadDetail": "广东省 广州市 天河区 广州珠村",
                "addressType": "2",
                "addressName": "广东省 广州市 天河区 广州珠村",
                "chemicalUnit": null,
                "totalWeight": 0,
                "totalVolume": 0,
                "loadCkeckUserId": 326,
                "loadCheckUserName": null,
                "loacCheckUserTel": null,
                "loadCheckTime": null,
                "loadCheckTotalWeight": null,
                "loadCheckTotalVolume": null,
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
                "transType": 2
            },
            "addressGoodsMes": [
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23967,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22524,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23966,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22523,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                },
                {
                    "weight": 0,
                    "volume": 0,
                    "baozhaung": {
                        "id": 23965,
                        "origId": "0Z6U1V51C3GU0YKRG7F00RG0AⅡ",
                        "billId": 9409,
                        "billAddressId": 22522,
                        "billUnitId": 14483,
                        "chemicalId": 72,
                        "chemicalName": "车用汽油或汽油",
                        "chemicalType": 3,
                        "chemicalItemNo": null,
                        "chemicalUnit": "吨",
                        "packLevel": 2,
                        "unionCode": "1203",
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
                    },
                    "bieming": null
                }
            ]
        }
    ],
    "shipBaseMes": {
        "origId": "0Z6U1V51C3GW",
        "billUnitId": 14483,
        "billId": 9409,
        "billNo": "20171020228221",
        "companyId": 990513,
        "bsUnitId": null,
        "unitName": "广东销售广州分公司",
        "unitType": 2,
        "contactPerson": "姜晨宇",
        "contactTel": "38018314",
        "fax": null,
        "remark": "接口同步数据",
        "createdUser": null
    },
    "ydh": "20171020228221"
}
```