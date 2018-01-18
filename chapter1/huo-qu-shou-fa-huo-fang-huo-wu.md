#### 获取收发货方货物

##### 接口地址

```
/app/dyBillShipReceiveUnit/getDyShipReceiveUnitAndDyBillChemical
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo | String | 运单号 | TRUE|
| unitType | Integer | 1:发货方；2:收货方 |TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |
| data| String | 响应数据 |
| id| Long| 货物ID |
| billId| Long| 运单ID |
| billAddressId| Long| 运单地址ID |
| billUnitId| Long| 运单收发货方ID |
| chemicalId| Long| 危化品ID |
| chemicalName| String | 危化品别名 |
| chemicalUnit| String | 货物单位 |
| chemicalType| Integer| 危化品类型 |
| chemicalItemNo| String | 响应数据 |
| packLevel| Integer| 包装级别 |
| unionCode| String | 联合国编号 |
| weight| String | 运单填写重量 |
| volume| String | 运单填写体积 |
| checkWeight| String |企业确认重量 |
| checkVolume| String | 企业确认体积 |
| loadCheckWeight| String | 司机确认重量 |
| loadCheckVolume| String | 司机确认体积 |
| transType| Integer| 1:  发货、装货2：收货、卸货 |
| checkTime| String | 企业确认时间 |
| chemicalTypeName| String | 危化品类型名称 |

##### 调用示例

```
/app/dyBillShipReceiveUnit/getDyShipReceiveUnitAndDyBillChemical
```

参数

```
{unitType:1,billNo:"20180118288944"}
```

响应示例

``` json
{
    "status": 1,
    "data": [
        {
            "id": 35469,
            "origId": "",
            "origChemicalId": "",
            "billId": 71347,
            "billAddressId": 33032,
            "billUnitId": 32643,
            "chemicalId": 2,
            "chemicalName": "别名2",
            "chemicalType": 1,
            "chemicalItemNo": 1,
            "chemicalUnit": "吨",
            "packLevel": 3,
            "unionCode": "0005",
            "weight": 5,
            "volume": 0,
            "driveMileage": "",
            "checkWeight": 5,
            "checkVolume": 0,
            "loadCheckWeight": "",
            "loadCheckVolume": "",
            "transType": 1,
            "chemicalTypeName": "1类",
            "chemicalAlias": "",
            "checkTime": "",
            "checkUserName": "",
            "checkUserTel": "",
            "checkRemark": ""
        },
        {
            "id": 35468,
            "origId": "",
            "origChemicalId": "",
            "billId": 71347,
            "billAddressId": 33032,
            "billUnitId": 32643,
            "chemicalId": 3,
            "chemicalName": "别名1",
            "chemicalType": 1,
            "chemicalItemNo": 1,
            "chemicalUnit": "吨",
            "packLevel": "",
            "unionCode": "0006",
            "weight": 5,
            "volume": 0,
            "driveMileage": "",
            "checkWeight": 5,
            "checkVolume": 0,
            "loadCheckWeight": "",
            "loadCheckVolume": "",
            "transType": 1,
            "chemicalTypeName": "1类",
            "chemicalAlias": "",
            "checkTime": "",
            "checkUserName": "",
            "checkUserTel": "",
            "checkRemark": ""
        }
    ],
    "message": "成功"
}
```