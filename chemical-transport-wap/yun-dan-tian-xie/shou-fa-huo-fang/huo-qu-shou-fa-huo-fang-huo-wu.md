#### 获取收发货方货物

##### 接口地址

```
/app/dyBillShipReceiveUnit/getDyShipReceiveUnitAndDyBillChemical/{billNo}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo | String | 运单号 | Y |
| unitType | Integer | 1:发货方；2:收货方 | N |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
/app/dyBillShipReceiveUnit/getDyShipReceiveUnitAndDyBillChemical/123456
```

参数

```
{unitType：1}
```

响应示例

``` json
[{
	"id": 70,
	"billId": null,
	"billAddressId": 47,
	"billUnitId": 31417,
	"chemicalId": 2930,
	"chemicalName": "丁硫醇",
	"chemicalType": 3,
	"chemicalItemNo": null,
	"chemicalUnit": "吨",
	"packLevel": 2,
	"unionCode": "2347",
	"weight": 6,
	"volume": 6,
	"driveMileage": null,
	"checkUserId": null,
	"checkUserName": null,
	"checkUserTel": null,
	"checkWeight": null,
	"checkVolume": null,
	"checkCompanyId": null,
	"checkCompanyName": null,
	"checkTime": null,
	"checkRemark": null,
	"loadCheckUserId": null,
	"loadCheckUserName": null,
	"loadCheckUserTel": null,
	"loadCheckWeight": null,
	"loadCheckVolume": null,
	"loadCheckTime": null,
	"loadCheckCompanyId": null,
	"loadCheckCompanyName": null,
	"loadCheckRemark": null,
	"transType": 1,
	"chemicalTypeName": null,
	"chemicalAlias": null
},
{
	"id": 69,
	"billId": null,
	"billAddressId": 46,
	"billUnitId": 31417,
	"chemicalId": 2928,
	"chemicalName": "3-溴丙炔",
	"chemicalType": 3,
	"chemicalItemNo": null,
	"chemicalUnit": "吨",
	"packLevel": 2,
	"unionCode": "2345",
	"weight": 5,
	"volume": 6,
	"driveMileage": null,
	"checkUserId": null,
	"checkUserName": null,
	"checkUserTel": null,
	"checkWeight": null,
	"checkVolume": null,
	"checkCompanyId": null,
	"checkCompanyName": null,
	"checkTime": null,
	"checkRemark": null,
	"loadCheckUserId": null,
	"loadCheckUserName": null,
	"loadCheckUserTel": null,
	"loadCheckWeight": null,
	"loadCheckVolume": null,
	"loadCheckTime": null,
	"loadCheckCompanyId": null,
	"loadCheckCompanyName": null,
	"loadCheckRemark": null,
	"transType": 1,
	"chemicalTypeName": null,
	"chemicalAlias": null
},
{
	"id": 68,
	"billId": null,
	"billAddressId": 46,
	"billUnitId": 31417,
	"chemicalId": 2933,
	"chemicalName": "亚硝酸丁酯",
	"chemicalType": 3,
	"chemicalItemNo": null,
	"chemicalUnit": "吨",
	"packLevel": 2,
	"unionCode": "2351",
	"weight": 1,
	"volume": 5,
	"driveMileage": null,
	"checkUserId": null,
	"checkUserName": null,
	"checkUserTel": null,
	"checkWeight": null,
	"checkVolume": null,
	"checkCompanyId": null,
	"checkCompanyName": null,
	"checkTime": null,
	"checkRemark": null,
	"loadCheckUserId": null,
	"loadCheckUserName": null,
	"loadCheckUserTel": null,
	"loadCheckWeight": null,
	"loadCheckVolume": null,
	"loadCheckTime": null,
	"loadCheckCompanyId": null,
	"loadCheckCompanyName": null,
	"loadCheckRemark": null,
	"transType": 1,
	"chemicalTypeName": null,
	"chemicalAlias": null
}]
```