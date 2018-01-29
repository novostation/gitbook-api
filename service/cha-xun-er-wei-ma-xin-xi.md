#### 查询二维码扫码的信息

##### 接口地址

```
/app/confirm/qrCodeInfo
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo | String | 运单号 | TRUE|
| billUnitId | String | 运单收发货方id | TRUE|
| billAddressId| String | 运单收发地址id | TRUE|
| addressType| Integer | 1: 发货、装货 2：收货、卸货 | TRUE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
|now | String | 当前时间 |
|billNo| String | 运单号|
|billUnitId | Long | 收货企业ID |
|unitName | String | 收发货方名称 |
|billAddressId| Long | 地址ID |
|roadDetail| String | 地址详情 |
|addressType| String | 1: 发货、装货 2：收货、卸货 |
| chemical| JSON| 货物 |
| id| Long | 货物id|
| chemicalName| String | 货物别名 |
| checkWeight| Float| 企业确认重量 |
| checkVolume| Float| 企业确认体积 |
| loadCheckWeight| Float| 司机确认重量 |
| loadCheckVolume| Float| 司机确认体积 |
| chemicalId| Long | 化学品id |
| unionCode| String | 化学品国际编号 |
| chemicalUnit| String | 化学品单位 |

##### 调用示例

```
url:/app/confirm/qrCodeInfo


参数：

{
	"data": {
		"billno": "20180111454511",
		"billUnitId": "0ZC6MQD2N7LW",
		"billAddressId": "0ZC6MQD2N7LZ",
		"addressType": "1"
	}
}
```

##### 响应示例
``` json
{
    "status": 1,
    "data": {
        "now": "2018-01-29 11:35:51",
        "unitName": "广州加德士",
        "billNo": "20180111454511",
        "chemical": [
            {
                "id": 31571,
                "origId": "A0ZC6MQD2N7LV0YKRG7F00RG0Ⅱ",
                "origChemicalId": "0ZC6MQD2N7LV",
                "billId": 68943,
                "billAddressId": 29001,
                "billUnitId": 28708,
                "chemicalId": 72,
                "chemicalName": "车用汽油或汽油",
                "chemicalType": 3,
                "chemicalItemNo": "",
                "chemicalUnit": "吨",
                "packLevel": 2,
                "unionCode": "1203",
                "weight": 32,
                "volume": 0,
                "driveMileage": "",
                "checkWeight": "",
                "checkVolume": "",
                "loadCheckWeight": 10086,
                "loadCheckVolume": 5,
                "transType": 1
            }
        ],
        "billUnitId": 28708,
        "addressType": 1,
        "roadDetail": "",
        "billAddressId": 29001
    },
    "message": "获取成功！！"
}
```


